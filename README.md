# 🛍️ AI-Powered Product Image Enhancer

This project provides a complete pipeline to process raw product images into enhanced, e-commerce-ready images using background removal, cropping, and AI-based image generation (Stable Diffusion inpainting).

---

## 🚀 Features

- ✅ Background removal using `rembg` API
- ✅ Cropping and resizing to square (1:1 aspect ratio)
- ✅ Automatic mask generation from transparency
- ✅ Image enhancement with **Stable Diffusion Inpainting**
- ✅ Generates 3 different image variants with plain white studio-style backgrounds

---

## 🧱 Project Structure
📁 root/
├── image_enhancer.ipynb # Colab notebook
├── README.md e
├── example_outputs/ # Folder for enhanced images 
└── requirements.txt # or local use

---

## 🛠️ Setup Instructions

### ✅ Google Colab (Recommended)
1. Open the `image_enhancer.ipynb` notebook in **Google Colab**.
2. Make sure GPU is enabled:  
   `Runtime > Change runtime type > Hardware Accelerator > GPU`
3. Upload your product image when prompted.
4. Enter your `rembg` API key (can be obtained at [https://www.rembg.cc](https://www.rembg.cc)).
5. Run the notebook to generate 3 enhanced image variants.
6. Download the results.

---

## 🔁 Steps Performed

1. **Upload Image**
   - Upload any product photo (preferably from [https://www.sabhyasha.com](https://www.sabhyasha.com)).

2. **Background Removal**
   - Background is removed using the `rembg` API.

3. **Square Cropping**
   - Image is center-cropped and resized to a perfect 1:1 square using `Pillow`.

4. **Mask Generation**
   - A mask is auto-generated from the transparent background to preserve the product and only modify the background.

5. **Stable Diffusion Inpainting**
   - Using `runwayml/stable-diffusion-inpainting`, the pipeline fills in a new background based on descriptive prompts.

6. **Prompt Variants**
   - The same product is placed in 3 white studio-style prompt environments with slight variations in lighting, shadow, and wording for diversity.

7. **Download Final Results**
   - Images are saved and can be downloaded in the final cell.

---

## ✨ Example Prompts Used

```text
1. a plain white studio background with soft diffused lighting, realistic shadow under the product, centered layout
2. a white seamless backdrop with high key lighting, clean environment, subtle shadows
3. product centered on a white background, diffused daylight, clean and minimal style, professional shoot
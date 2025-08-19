# AI Photoshoot Studio 🎨

**Your Personal AI Art Director. Turn simple text prompts into stunning, pose-controlled visuals with the magic of ControlNet.**

[![Python Version](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/downloads/)
[![Made with Diffusers](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Diffusers-orange)](https://github.com/huggingface/diffusers)
[![Powered by PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?&style=flat&logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![Gradio UI](https://img.shields.io/badge/Gradio-UI-ff7600)](https://gradio.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 🎬 Quick Look

Watch a quick demo of how the AI Photoshoot Studio can transform your ideas into reality.

<p align="center">
  <img src="https://raw.githubusercontent.com/Vishisht16/AI-Photoshoot-Studio/main/trial.gif" alt="AI Photoshoot Studio Demo" width="80%">
</p>

---

## 🌟 About The Project

This isn't just another text-to-image generator. The **AI Photoshoot Studio** is a comprehensive and interactive web application designed to give you, the user, fine-grained artistic control over the image generation process.

The project's core philosophy is to elevate the user from a passive *prompter* to an active **Art Director**. By integrating the powerful **ControlNet** framework, this studio allows you to dictate the exact pose and structure of the people in your images, opening up a new world of creative possibilities.

## ✨ Key Features

-   **Dual Generation Modes:**
    -   **Standard Mode:** Don't have a specific pose in mind? No problem! Just write a prompt and generate incredible images like any standard text-to-image model. Perfect for creating images of animals, landscapes, or objects.
    -   **ControlNet Mode:** Upload an image of a person, and the studio will use their **exact pose** as a blueprint for your new creation.

-   **📸 Precise Pose Control:** Leveraging the **OpenPose** ControlNet model, you can copy a pose from any photograph and apply it to a new character described in your prompt.

-   **🎭 "Digital Doppelgänger" Face Preservation:** Want the generated character to look like the person in your uploaded photo? Our advanced inpainting workflow intelligently preserves the facial features from the control image, creating a "digital look-alike" in a completely new scene.

-   **🔧 Advanced Creative Controls:**
    -   **Scheduler Selection:** Experiment with different denoising algorithms (like DDIM, PNDM) to achieve unique textures and styles.
    -   **Inference Steps & CFG Scale:** Fine-tune the generation process for more detail or more creative freedom.

-   **👨‍💻 Intuitive & User-Friendly UI:**
    -   A sleek, professional interface with a built-in user manual.
    -   Helpful features like auto-filling negative prompts and resetting settings to default.

## 🛠️ Tech Stack & Architecture

This project is built with modularity and abstraction in mind, ensuring the code is clean, scalable, and easy to understand.

-   **Backend:** Python
-   **AI & Deep Learning:** PyTorch, Hugging Face `diffusers`, `transformers`
-   **Control Framework:** ControlNet (OpenPose)
-   **Core Models:** Stable Diffusion v1.5
-   **UI Framework:** Gradio
-   **Computer Vision:** OpenCV, MediaPipe

### 📁 Folder Structure

The project maintains a clean separation of concerns within the Colab Notebook once all cells are run:

```
├── 📁 app/               # Contains all front-end and Gradio UI logic
│   ├── app_gradio.py    # Main UI builder and event handling
│   └── ui_components.py # Defines the UI layout and components
│
├── 📁 core/              # The "Brain" of the application
│   ├── pipeline_manager.py # Manages loading all AI models and pipelines
│   └── utils.py         # Helper functions for tasks like face detection
│
├── 📄 app.py              # The single entry point to launch the application
```

---

## 🚀 Getting Started (The Easy Way)

The best way to run this project is on **Google Colab**, which provides a FREE T4 GPU.

**Here are the step-by-step instructions from the provided notebook:**

1.  **Open the Notebook:** Launch the `.ipynb` file in Google Colab.s
2.  **Select GPU:** In the menu, go to `Runtime` -> `Change runtime type` and select **T4 GPU** from the dropdown.
3.  **Run the Pip Install Cell:** The first code cell installs all the necessary libraries. Run it.
4.  **IMPORTANT: Restart the Runtime:** After the installation finishes, go to `Runtime` -> `Restart session`. This is crucial for Colab to recognize the new libraries.
5.  **Run All Cells:** Now, go to `Runtime` -> `Run all`. This will write the Python files, download the AI models (this may take 5-10 minutes on the first run), and launch the app.
6.  **Browse the URL:** At the end of the output, you will see a public Gradio URL (ending in `.gradio.live`). Click on it to open the AI Photoshoot Studio in a new tab!
7.  **When Done:** To save resources, go to `Runtime` -> `Disconnect and delete runtime`.

## License

Distributed under the MIT License. See `LICENSE` file for more information.
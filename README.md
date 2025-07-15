# 🎨 Cartoon-Based Story Generator

**Cartoon-Based Story Generator** is a Python script (Jupyter Notebook) that leverages OpenAI's powerful **GPT-4** model to craft engaging cartoon stories and **DALL-E** to generate a unique cartoon image for each scene. Perfect for creative writing, educational content, or just for fun!

---

## 🚀 Features

* **Story Generation:** Generates imaginative and coherent cartoon stories based on your specific prompts, powered by OpenAI's GPT-4.

* **Image Generation:** Creates a distinct, cartoon-style image for every scene (paragraph) of the generated story using OpenAI's DALL-E.

* **Interactive Experience:** Provides a seamless, interactive environment within Google Colab to input prompts, execute the script, and view the generated stories and images instantly.

---

## ✅ Prerequisites

Before you dive in, make sure you have the following ready:

* **Python 3.x:** The notebook is written in Python.

* **OpenAI API Key:** An active OpenAI API key is required, with access enabled for both GPT-4 and DALL-E models.

* **Google Colab Environment:** The notebook is optimized for Google Colaboratory, which simplifies setup and execution.

---

## 📦 Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/Cartoon-Based-Story-Generator.git](https://github.com/your-username/Cartoon-Based-Story-Generator.git)
    cd Cartoon-Based-Story-Generator
    ```

2.  **Open the notebook in Google Colab:**
    Upload the `a_cartoon_based_story_generator.ipynb` file to your Google Drive and open it using Google Colaboratory.

3.  **Install dependencies (within Colab):**
    The very first cell in the notebook will automatically handle the installation of necessary Python libraries:
    ```bash
    !pip install openai==0.28
    !pip install requests
    ```

---

## 🖥️ How to Use

1.  **Upload your OpenAI API Key:**
    Execute the cell containing the `upload_api_key()` function. A prompt will appear, guiding you to upload your API key file (e.g., `api_key.txt`). This file should strictly contain only your OpenAI API key.

2.  **Enter your story prompt:**
    Once your API key is successfully uploaded, you'll be prompted to provide a creative prompt for your cartoon story. For example:
    `Enter a prompt for your cartoon story: Brian, the CEO of UHC announced that he would pay all the customer's health insurance - with no denials. As he said this, from out the window, a roast pig flew across the sky. Brian was shocked. He turned to his fellow shareholders and said "Maybe later."`

3.  **View the generated story and images:**
    The notebook will then process your prompt, generate the complete story, and subsequently create and display a unique cartoon image for each paragraph (scene) of your story.

---

## 🧰 Code Structure

* `a_cartoon_based_story_generator.ipynb`: This is the core Jupyter Notebook, containing all the Python code for story and image generation.

### Key Functions Explained:

* `upload_api_key()`: A utility function designed to securely handle the upload of your OpenAI API key within the Colab environment.

* `generate_story(prompt)`: Takes your text prompt and interacts with `openai.ChatCompletion.create` using the "gpt-4" model to produce the cartoon story.

* `generate_image(scene_description)`: Utilizes `openai.Image.create` with OpenAI's DALL-E model to generate an image URL based on a scene description, then downloads and displays the image.

---

## 📸 Example Output

(As images are dynamically generated, actual screenshots would typically be embedded here in a live `README.md`. Below is a description of the expected output format.)

The execution will first display the entire generated story. Following this, for each distinct scene (paragraph) in the story, you will see:
Scene 1: [First paragraph of the story]
Image for Scene 1: https://openai.com/index/dall-e-2/ (Example URL, actual will vary)
[Displayed Image]

Scene 2: [Second paragraph of the story]
Image for Scene 2: https://openai.com/index/dall-e-2/ (Example URL, actual will vary)
[Displayed Image]
...and so on for every scene.
---

## ⚠️ Error Handling

The script incorporates basic error handling to manage common issues:

* `openai.error.OpenAIError`: Catches and reports errors directly from the OpenAI API (e.g., issues with your API key, rate limiting).

* General `Exception`: Provides a fallback for other unexpected errors that might occur during the story or image generation process.

---

## 👋 Contributing

Contributions are welcome! Feel free to fork this repository, open issues for suggestions or bugs, and submit pull requests to enhance the story and image generation capabilities.

---

## 📜 License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).

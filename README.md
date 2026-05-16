# Purim Costume AI Generator

A beginner-friendly Jupyter Notebook project that converts a portrait photo into a new costume-style image using AI.

## What this project does

- Lets you choose a costume from a list of ideas
- Uploads a portrait image from your computer
- Uses OpenAI to generate a text description of the portrait
- Builds a prompt for a costume-style image using the portrait description + chosen costume
- Sends that prompt to Replicate AI models to generate a new image
- Saves the generated results into the `customs/` folder

## Who is this for?

This project is perfect for beginners who want to learn how to combine:
- Jupyter notebooks
- image handling in Python
- OpenAI text/image generation
- Replicate image synthesis
- environment variables and API keys

## Files and folders

- `src/purim.ipynb` - main notebook with the project workflow
- `customs/` - output folder for generated costume images
- `images/` - place your portrait photo here before processing
- `src/.env` - store API keys here (not included in source control)

## Prerequisites

- Python 3.11+ installed
- Jupyter Notebook or Jupyter Lab installed
- `pip` available
- OpenAI API key
- Replicate API key

## Setup

1. Open a terminal in the project root:

```powershell
cd c:\Users\User\Desktop\codes\purim
```

2. Install the required Python packages:

```powershell
pip install openai replicate python-dotenv pydantic ipython
```

3. Create a `.env` file in the `src/` folder with your API keys:

```text
OPENAI_API_KEY=your_openai_api_key_here
REPLICATE_API_KEY=your_replicate_api_key_here
```

4. Copy a portrait image into the `images/` folder or use the notebook prompt to load it from any path.

## Running the project

1. Start Jupyter Notebook:

```powershell
jupyter notebook src/purim.ipynb
```

2. Open `src/purim.ipynb` in your browser.
3. Run each cell in order.
4. When prompted, provide the path to your portrait image and choose a costume from the list.

## How it works

1. A list of costume ideas is created in the notebook.
2. The notebook copies your portrait image into `images/`.
3. It asks OpenAI to describe the portrait image.
4. You choose a costume.
5. It sends a combined prompt to OpenAI to build a realistic output prompt.
6. It calls Replicate to generate one or more new images.
7. The generated result is saved into `customs/` and displayed in the notebook.

## Tips for beginners

- Run the notebook one cell at a time.
- Keep your API keys private and do not share them.
- If the notebook shows an error, read the message and check the previous cell.
- Make sure your image path is correct and the file is accessible.

## Notes

- The project uses `gpt-5-mini-2025-08-07` in the notebook for text/image prompt creation.
- The notebook also uses Replicate models like `black-forest-labs/flux-kontext-pro` and `google/nano-banana-2`.
- If you want to add more costumes, edit the `list_of_customs` list in `src/purim.ipynb`.

---

Feel free to experiment by adding more costumes, changing the prompt text, or trying different images.
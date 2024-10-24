# How about animated Memoji in Lottie?

## Background

I couldn't find a way to embed animated stickers from iMessage into websites.
So, I wrote my own solution. I hope it helps you too!

## Introduction

This project allows you to convert animated Memoji from `.mov` format to Lottie.
Lottie is a powerful animation format that is well-suited for web applications
because it supports transparent backgrounds and is lightweight. The default
export from iMessage is in `.mov` format, which not only has a dark background
but is also not intended for direct use on websites. This project aims to
provide a better alternative by converting those animations into the Lottie
format.

## Features

- Convert `.mov` animated Memoji to Lottie format.
- Remove dark backgrounds using the OpenCV library.
- Convert each frame to `.webp` format for efficient web use.
- Generate a Lottie JSON file ready for embedding in web projects.

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/machnevegor/memoji
   cd memoji
   ```

2. Install the dependencies using Poetry:
   ```bash
   poetry install
   ```

3. Create your animated Memoji in iMessage. For guidance, check out
   [this support article](https://support.apple.com/en-us/111115).

4. Export the Memoji as a `.mov` file to the [data/](data) directory.

5. Open the Jupyter Notebook [notebook.ipynb](notebook.ipynb).

6. Update the `INPUT_VIDEO` and `OUTPUT_JSON` paths in the notebook to point to
   your `.mov` file and desired output JSON file.

7. Run the cells in the notebook to process the animation.

8. Check the output: Review the generated JSON file to ensure it meets your
   quality standards.

9. Copy the generated JSON file to your website. Enjoy!

## Important Notes

- The conversion process includes a compression step when generating `.webp`
  files. Please note that this process is **not lossless**, meaning some quality
  may be reduced. Make sure to review the output to ensure it meets your needs.
- If you encounter any issues or have questions, feel free to open an issue in
  this repository.

## Contributing

Contributions are welcome! If you have suggestions or improvements, please
create a pull request or open an issue.

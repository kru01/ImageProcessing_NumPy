<a name="readme-top"></a>

# ImageProcessing with NumPy

- Project from HCMUS's 2023 Applied Mathematics and Statistics course.
- ***Disclaimer: This program only supports `RGB` color model.*** Others such as `RGBA`, `CMYK`, or `HSL`, etc. might produce questionable results or not work at all.

## Content

- `lab03_project02.ipynb` contains all the tasks and requirements of the project.
- `Report.pdf` includes my documentation for all the algorithms and required tasks.
   - First full-fledged report written in LaTeX, quite a pain but also very hype.
- `sample` folder holds the pictures that were used during implementation and documentation.
- `figures` folder includes every figure featured in `Report.pdf`.

### `ImageProcessing.ipynb`

- The `Miscellaneous functions` exist solely for handling inputs and outputs, they **definitely are NOT** the main focus of the notebook.
   - I recommend skipping them entirely and just reading the descriptions in the `Main function` section.
- `Past implementations` at the bottom of the notebook are not entirely unusable, they are only inferior to the current implementation.
   - I think they are worth keeping to reflect the growth of the project.

## Getting Started

### Prerequisites

- Any IDE, preferably VSCode.
- Python 3.11 and Jupyter package.
  - Alternatively, the `.ipynb` file can be run on Google Colab or Anaconda.
- Everything from the `Import libraries and essential functions` section of the notebook.

### Installation

- Clone the repo.

## Usage

- **Make sure `Import libraries and essential functions` is run at least once.**
- For saving, 2 supported filetypes are `.png` and `.pdf`.
   - *To opt out of saving, either leave the input `blank` or mess it up.*
- **Inputs must follow the format of `<img_file> <function> <parameters>`. Inputs do NOT need to be fully complete.** As long as the `<img_file>` is correct, the `<function>` and **especially `<parameters>` are optional.** The `<parameters>` varies across functions, which is noted below.
   - Every input concerning `tuple`s must be in the format of `<Y>x<X>`. E.g., `420x690` means `y=420,x=690` or `height=420,width=690`.
   - E.g., `img.jpg 7 0.5 600x400`, `img.png 7 100`, `img.jpg 7`, `img.png 4`, etc.
### Input notes

0. **All** - Inputting only the `<img_file>` will default to this function. `<parameters>` is NOT required.
1. **Brightness** - `<factor>`, `float` denoting how much the brightness will be adjusted.
   - E.g., `-0.5` darkens by `50%`, `0.35` brightens by `35%`.
1. **Contrast** - `<factor>`, `float` denoting how much the contrast will be adjusted.
   - E.g., `-0.5` adjusts by `-127=int(-0.5*255)`, `0.35` adjusts by `89=int(0.35*255)`.
1. **Flipping** - `<axis>`, `int` representing the direction to flip the image.
   - `0` for vertical, `1` for horizontal, `<blank>` for both.
1. **Grayscale and Sepia** - `0` for grayscale, `1` for sepia, `<blank>` for both.
   - After `0` for grayscale, `0` for average, `1` for luminosity, `<blank>` for both.
1. **Blurring and Sharpening** - `0` for blurring, `1` for sharpening, `<blank>` for one execution of each.
   - After `0` or `1`, input an `int` denoting how many times to blur or sharpen.
1. **Center cropping** - Two methods of inputting.
   - `tuple` of `(height, width)` denoting the dimension of the cropped image. E.g., `420x690`, `727x135`.
   - `float` denoting the ratio between the cropped and the original image. E.g., `0.5` means `50%` of the original image.
1. **Circle cropping** - Two parameters.
   1. `<radius>` - The domains of this value produce different outcomes.
      - `int (rad > 1)` denoting the radius of the cropped image.
      - `<float> (0 < rad <= 1)` denoting ratio between the cropped and the original image.
      - Leave `<blank>` or `0` to use the smallest distance between the center and image walls.
   1. `<center>`, `tuple (y, x)` denoting the coordinate of the center of the cropped image.
      - Leave `<blank>` to use the center of the original image.
1. **Cross Ellipses cropping** - Two parameters.
   - *To get the best result, everything should be left `<blank>`.*
   1. `<radius>` - The datatypes of this value produces different outcomes.
      - `tuple (rad_y, rad_x)` denoting the radii of the cropped image.
      - `int` denoting the radius of the cropped image.
      - Leave `<blank>` or `0` to use the optimal dimension.
   1. `<center>` - `tuple (y, x)` representing the coordinate of the center of the cropped image.
      - Leave `<blank>` to use the center of the original image.

## Built With

[vscodeicon]: https://skillicons.dev/icons?i=vscode&theme=dark
[vscodeurl]: https://code.visualstudio.com/

[pythonicon]: https://skillicons.dev/icons?i=py&theme=dark
[pythonurl]: https://www.python.org/

[jupytericon]: https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg
[jupyterurl]: https://code.visualstudio.com/docs/datascience/jupyter-notebooks

[windowsicon]: https://cdn.jsdelivr.net/gh/devicons/devicon/icons/windows8/windows8-original.svg
[windowsurl]: https://www.microsoft.com/en-us/windows/

| [![VSCode][vscodeicon]][vscodeurl] | [![Python][pythonicon]][pythonurl] | [![Jupyter][jupytericon]][jupyterurl] | [![Windows][windowsicon]][windowsurl] |
| :-: | :-: | :-: | :-: |
| 1.80.1 | 3.11.4 | VSCode | &nbsp;&nbsp; 11 &nbsp;&nbsp; |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

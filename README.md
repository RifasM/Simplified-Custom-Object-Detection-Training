# Custom Object Detection Simplified

## How to Run
Use TensorFlow 1.15 \
Requires [Python 3.5+](https://www.python.org/ftp/python/3.6.4/python-3.6.4.exe).
### Fork and clone this repository to your local machine.
```
https://github.com/RifasM/Simplified-Custom-Object-Detection-Training
```
### Install required libraries
`pip3 install -r requirements.txt`


### Step 1: Annotate some images
- Save some pictures with your custom object(s), ideally with `jpg` extension to `./data/raw` directory.(>20 Suggested)
- Resize those pictures to uniformed size. e.g. `(800, 600)` using the command
```
python resize_images.py --raw-dir ./data/raw --save-dir ./data/images --ext jpg --target-size "(800, 600)"
```
Resized images can now be found in `./data/images/`
- Split those files into two directories, `./data/images/train` and `./data/images/test`

- Annotate these resized images with [labelImg](https://tzutalin.github.io/labelImg/) to generate `xml` files inside `./data/images/train` and `./data/images/test` folders. 

*Tip: Use available shortcuts (`w`: draw box, `d`: next file, `a`: previous file, etc.) to accelerate the annotation.*

- Commit and push your annotated images and xml files (`./data/images/train` and `./data/images/test`) to your forked repository.


### Step 2: Open `tensorflow_object_detection.ipynb` on [Jupyter Notebook](https://jupyter.org/install) or [Colab notebook](https://colab.research.google.com/)
- Replace the repository's url to yours and run it.
- Follow the Instructions on the Notebook

Machine Learning
===
This folder contains all relevant resources for the Machine Learning workshops at WAKE.

If you think something could be improved, or spot any errors in any of the content, please submit a pull request to fix 
it -- all contributions are welcomed!

Contents
---
These are listed in the intended order of study, largely set by pre-requisites.

**Session 1:** From linear models to deep learning
- The main focus of this session is the 'Linear models to ML' notebook (see `s1_linearmodelstoml_full.ipynb`).
  The additional gradient descent and loss functions notebooks require some concepts from this, so it is encouraged to
  familiarise yourself beforehand if self-studying this course.
- In the notebooks, I also suggest relevant times to check out the other notebooks.

**Session 2:** Machine learning for modern astronomy
- Building research-ready ML code using modern frameworks

Each session is contained within its own folder for ease of organisation - each session contains:
- Slides 
- Session notebooks with elements missing for you to write, tweak, and experiment with
- A 'solution' notebook fully filled in for you to refer to
- Additional resources for you to read more about the content of each session

Installation and usage
---
All package requirements are contained in the `requirements.txt` file - to install them, execute the following commands
below in your terminal/shell from the `machine_learning` subfolder. 
This command should work the same regardless of your chosen operating system.
Please note that the notebooks need Python 3 - all standard distributions should (hopefully) contain this now.

```shell
pip install --upgrade pip setuptools wheel
pip install -r requirements.txt
```
You will need at least 600MB of free space to install the required packages. This can be done via 
[Google Colab](https://research.google.com/colaboratory/) or other online-hosted Jupyter notebook instances if this is 
an issue.

To access the Jupyter notebooks, run the below in your terminal:
```shell
jupyter lab
```
This will spawn a Jupyter server on your local machine - copy the URL (looks like 
`http://localhost:8888/lab?token=[your_token]`) into your web browser to access the notebook interface.
When you've finished using the notebook, press `Ctrl-C` in the terminal and answer `y` to the shutdown message.

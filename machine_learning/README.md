Machine Learning
===
This folder contains all relevant resources for the Machine Learning workshops at WAKE.

If you think something could be improved, or spot any errors in any of the content, please submit a pull request to fix 
it -- all contributions are welcomed!

Contents
---
**Session 1:** From linear models to machine learning  
**Session 2:** Machine learning for modern astronomy

Each session is contained within it's own folder for ease of organisation - each session contains:
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
You will need at least 600MB of free space to install the required packages.

To access the Jupyter notebooks, run the below in your terminal:
```shell
jupyter-lab
```
This will spawn a Jupyter server on your local machine - copy the URL (looks like 
`http://localhost:8888/lab?token=[your_token]`) into your web browser to access the notebook interface.
When you've finished using the notebook, press `Ctrl-C` in the terminal and answer `y` to the shutdown message.

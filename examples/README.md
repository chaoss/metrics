# Examples of implementations for metrics

Notebooks, built on top of data collected by Perceval,
for illustrating how to compute metrics:

* [Code Commits](Code_Commits.ipynb),
includes generation of file [git-commits.json],
with a Perceval dump of a git repository, as data source.

# How to run the notebooks

First of all, you need a Python3 environment with certain modules installed
(it is recommendable to use a virtual environment,
  see [Creation of virtual environments](https://docs.python.org/3/library/venv.html)).
To install the modules, just use pip3:

```bash
$ pip install jupyter
$ pip install pandas
$ pip install perceval
```

(check at the begining of each notebook just in case more modules need to be installed).

To run the notebook, once the modules above are installed, run:

```
jupyter notebook Code_Commits.ipynb
```

Of course, instead of `Code_Commits.ipynb` you can load any other notebook.
This will launch the Jupyter kernel, and will open your default browser
with the notebook loaded. More detailed instructions can be found in
[Introducing the Notebook Server’s Command Line Options](Introducing the Notebook Server’s Command Line Options).

Once you have the notebook in your browser, you can execute the selected cell
by clicking \[CTRL\]\[Enter\], or \[Shift\]\[Enter\]. In the latter case,
the current cell will be run, and the next one will be selected.
For selecting any cell, just click on it.

So, if you want to execute the whole dashboard, just select the first cell,
and click \[Shift\]\[Enter\] until you're done.
You can also click on the Cell menu, and select "Run All",
which will also run all the cells in the notebook.
More details can be found in [Executing a notebook](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/execute.html#executing-a-notebook)

If you want to modify any cell, just click on it, look for the cursor,
and start writing.

If you want more details and context about Jupyter notebooks, have a look at
[Jupyter Notebook Tutorial](https://www.datacamp.com/community/tutorials/tutorial-jupyter-notebook).

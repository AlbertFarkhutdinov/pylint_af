# pylint_af

![GitHub repo size](https://img.shields.io/github/issues/AlbertFarkhutdinov/pylint_af)
![PyPI version](https://img.shields.io/pypi/v/pylint-af)
![GitHub contributors](https://img.shields.io/github/contributors/AlbertFarkhutdinov/pylint_af)
![GitHub stars](https://img.shields.io/github/stars/AlbertFarkhutdinov/pylint_af)
![GitHub forks](https://img.shields.io/github/forks/AlbertFarkhutdinov/pylint_af)
![GitHub licence](https://img.shields.io/github/license/AlbertFarkhutdinov/pylint_af)

`pylint_af` is a Python package that allows you to check the Python code for compliance with PEP8.

## Prerequisites

Before you begin, ensure you have installed the latest version of Python.

## Installing `pylint_af`

To install `pylint_af`, follow these steps:

Linux and macOS:
```
pip3 install pylint-af
```

Windows:
```
pip install pylint-af
```
## Using `pylint_af`

There are examples of how to use `pylint_af`. 

To use the `PyLinter` class, import it as shown below:

```
>>> from pylint_af import PyLinter
```

### Simple checking without additional options:

```
>>>  PyLinter().check()

--------------------------------------------------------------------
Your code has been rated at 10.00/10 (previous run: 10.00/10, +0.00)

```

### Simple checking with printed pylint options:

```
>>>  PyLinter(is_printed=True).check()
--ignore-imports=yes
***
--------------------------------------------------------------------
Your code has been rated at ...

```

Here `***` is the list of inspected files.

### Example of checking with ignored pylint statements. 

```
>>>  PyLinter(is_printed=True, ignored_statements={'C0114'}).check()
--ignore-imports=yes
--disable=C0114
***
--------------------------------------------------------------------
Your code has been rated at ...

```

See [pylint documentation](https://docs.pylint.org/en/latest/technical_reference/features.html)
to study the full list of pylint statements. 

### Example of checking with ignored paths. 

```
>>> PyLinter(is_printed=True, ignored_paths={'example'}).check()
--ignore-imports=yes
--disable=C0114
***
--------------------------------------------------------------------
Your code has been rated at ...

```
Here `***` is the list of all inspected files 
in the current work directory except files in 'example' folder.

### Checking in other directory. 

```
>>> PyLinter(root_directory='C:\\other').check()
--------------------------------------------------------------------
Your code has been rated at ...

```

## Contributing to `pylint_af`
To contribute to `pylint_af`, follow these steps:

1. Fork this repository.
2. Create a branch: `git checkout -b <branch_name>`.
3. Make your changes and commit them: `git commit -m '<commit_message>'`
4. Push to the original branch: `git push origin <project_name>/<location>`
5. Create the pull request.

Alternatively see the GitHub documentation on [creating a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).

## Contributors

* [@AlbertFarkhutdinov](https://github.com/AlbertFarkhutdinov) 

## Contact

If you want to contact me you can reach me at `albertfarhutdinov@gmail.com`.

## License
<!--- If you're not sure which open license to use see https://choosealicense.com/--->

This project uses the following license: [MIT License](https://github.com/AlbertFarkhutdinov/pylint_af/blob/main/LICENSE).
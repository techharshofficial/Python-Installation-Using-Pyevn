
# How to Install Multiple Python Versions on your Computer and use them with VSCode




## Installation


```bash
  xcode-select --install
```
Before installing pyenv on macOS, you need to have the Xcode command line tools installed. This step ensures you have the necessary tools for building and compiling software on macOS.



```bash
  brew install openssl readline sqlite3 xz zlib
```
These dependencies are required for building Python and other packages. Homebrew is a package manager for macOS, and this step ensures that the necessary libraries are available.



### Installing pyenv on macOS can be done in two ways
#### Way 1
Update Homebrew and then install pyenv:

```bash
  brew update
  brew install pyenv
```
And after the installation has finished successfully, enter the following to add the pyenv to your $PATH and start pyenv when a new terminal window is opened
```bash
  echo 'eval "$(pyenv init --path)"' >> ~/.zshrc
```

#### Way 2
Alternatively, you can clone pyenv directly from the GitHub repository:
```bash
  git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```
After cloning, add pyenv to your $PATH and enable it to start with a new terminal window:
```bash
  echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
  echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
  echo 'eval "$(pyenv init --path)"' >> ~/.zshrc
```

Run the following command to verify that pyenv is correctly installed:\
This checks if pyenv is available and functioning within your shell.

```bash
  pyenv
```

List all available Python versions that can be installed using pyenv:

```bash
  pyenv install -l
```


Install a specific Python version (replace 3.12.1 with the version you want):
```bash
  pyenv install 3.12.1
```

hList all the Python versions you have installed using pyenv:
 
```bash
  pyenv versions
 
```

Set a global Python version to be used by default:

```bash
  pyenv global 3.12.1
```

Check if the correct Python version is now the active one:\
This step confirms that the installation was successful.

```bash
  python -version
```

or

```bash
  python -V
```
### Set a specific Python version for a project
If you want to set a specific Python version for a particular project, follow these steps:
\
Install Python version 3.11.0 using pyenv
```bash
  pyenv install 3.11.0
```
List installed Python versions
```bash
  pyenv versions
```
Set Python version 3.11.0 as the local version for the current project
```bash
  pyenv local 3.11.0
```
List all files in the current directory, including hidden files
```bash
  ls -a
```
Display the contents of the .python-version file in the current directory
```bash
  cat .python-version
```
Run a Python script named hello.py using the configured Python version
```bash
  python hello.py
```
Replace "3.11.0" with the desired Python version for your project. The .python-version file is created in your project directory, specifying the Python version for that project.

These steps provide a comprehensive guide for installing and managing multiple Python versions on your macOS system using pyenv and integrating it with Visual Studio Code.
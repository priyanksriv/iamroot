## WINDOWS SUBSYSTEM FOR LINUX (WSL)


#### links
  
- [Understanding what is WSL](https://learn.microsoft.com/en-us/windows/wsl/about)

- [Installation](https://learn.microsoft.com/en-us/windows/wsl/install)

- [Useful WSL Commands](https://learn.microsoft.com/en-us/windows/wsl/basic-commands)

- [Managing Disk Space](https://learn.microsoft.com/en-us/windows/wsl/disk-space)

- [MS Windows Terminal](https://learn.microsoft.com/en-us/windows/wsl/setup/environment#set-up-windows-terminal); [Video Tutorial](https://www.youtube.com/watch?v=2dsnwlnNBzs)

- [Using Linux GUI apps](https://learn.microsoft.com/en-us/windows/wsl/tutorials/gui-apps); [Video Tutorial](https://www.youtube.com/watch?v=kC3eWRPzeWw)

- [Adjusting case-sensitivity](https://learn.microsoft.com/en-us/windows/wsl/case-sensitivity)

- [Useful things to do in WSL](https://www.youtube.com/watch?v=qYlgUDKKK5A); note: ignore the GUI apps instructions, not needed anymore.

- todo
	- scrolling in vim window
	- disabling sound
	- install eza (a better ls/exa)
	 sudo apt install unzip
	
- more
sudo apt install libopencv-*	
OR
	sudo apt install libgtk2.0-dev
	sudo apt install pkg-config

sudo apt install sqlite3
	- git-lfs: https://github.com/git-lfs/git-lfs/blob/main/INSTALLING.md
	- tmux (with wsl - https://deliciousbrains.com/tmux-for-local-development/#install-tmux-windows)
	- git
		checkout lazygit
		git delta - better git diff https://www.youtube.com/watch?v=91p1Fp7Db5c
	- neovim
		https://www.youtube.com/watch?v=stqUbv-5u2s
		https://www.youtube.com/watch?v=hnTXJGm8VBA (beginner)
		astrovim - autoconfig https://astronvim.com/
	- fzf (fuzzy finder)

=======================================


vscode ext	
excel viewer (done)
Tabnine (autocomplete)
Prettier
Python Docstring Generator
Python indent
Yaml to Json
Trailing Spaces
Visual Studio IntelliCode
GitLens
Gitlab Workflow


py poetry
https://python-poetry.org/
https://ritza.co/articles/gen-articles/pipenv-vs-virtualenv-vs-poetry-vs-pyenv-vs-pip
https://www.youtube.com/watch?v=0f3moPe_bhk
https://www.youtube.com/watch?v=Qks3eqlImy8
	
	
python tools
black 	 : code formatter
isort 	 : imports sorter
flake8	 : static analysis --> pep8-naming, flake8-bugbear, flake8-docstrings
mypy 	 : type checking analysis
pytest	 : functional testing (alternative to unittest)
coverage : measuring test coverage (enable it pytest via pytest-cov)

-- adding devtools via poetry:
poetry add pytest@latest pytest-cov --dev
poetry add black isort mypy --dev
poetry add flake8 pep8-naming flake-docstrings flake8-bugbear --dev

-- configuring dev tools via pyproject.toml
[tool.black]
line-length = 160
target-version = ["py-310"]

[tool.isort]
profile = "black"
skip_gitignore = true

[tool.coverage.run]
branch= true

[tool.coverage.mypy]
exclude = ".cache/*"

-- check if flake8 supports pyproject.toml, else in setup.cfg
[flake8]
extend-ignore = E203,E501,W503
max-complexity = 10
extend-exclude = .cache/

-- gitignore -> in .gitignore/.p4ignore
note: poetry.lock SHOULD be included in repo

*.py[cod]
__pycache__/
__pypackages__/
*.egg-info/
.mypy_cache/
.cache
.cache/
.coverage
.coverage.*
cover/
htmlcov/
coverage.xml
junit.xml
dist/
sdist/
releases/
_build
_html
env/
venv/
.venv


https://www.digitalocean.com/community/tutorials/how-to-develop-a-docker-application-on-windows-using-wsl-visual-studio-code-and-docker-desktop
https://learn.microsoft.com/en-us/windows/wsl/networking

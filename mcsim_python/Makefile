
.PHONY: environment remove-env install uninstall test # .PHONY is something we can add when our target dependencies are not files.

MODULE=mcsim
ENVIRONMENT=chem274A_lab1

environment: remove-env	## create a new environment using python 3.9 called chem274A_lab1
	conda create -n $(ENVIRONMENT) "python=3.9" --yes
	conda install -c conda-forge notebook nbconvert numpy matplotlib pytest-cov pandas --name $(ENVIRONMENT) --yes

remove-env: ## remove the environment chem274A_lab1
	conda remove --name $(ENVIRONMENT) --all --yes


install: uninstall ## install the package to the active Python's site-packages
	pip install .

dev-install: uninstall ## install the package so that changes can easily be made to the package
	pip install -e .

uninstall: ## uninstall the package
	pip uninstall --yes $(MODULE)

test: ## perform the tests written in the Python code with notes on whether tests pass or not
	pytest -v

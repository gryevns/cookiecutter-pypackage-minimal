init:
ifndef VIRTUAL_ENV
    $(error Not running inside virtualenv)
endif
    pip install -r requirements.txt

style:
    flake8 --ignore F401,E501 .
    xenon --max-absolute B --max-modules A --max-average A .

test: style
    py.test tests

coverage:
    py.test --cov={{cookiecutter.package_name}} tests/

.PHONY: init test coverage style

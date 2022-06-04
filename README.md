# luhn-formula
Another Python ID validator and check digit generator package based on Luhn's formula :wink:. Luhn Formula was designed to protect against accidental input errors.

[![Python package](https://github.com/code-127/luhn-formula/actions/workflows/python-package.yml/badge.svg)](https://github.com/code-127/luhn-formula/actions/workflows/python-package.yml)
[![Python 3.8](https://img.shields.io/badge/python-3.8-blue.svg)](https://www.python.org/downloads/release/python-380/)
[![Python 3.9](https://img.shields.io/badge/python-3.9-blue.svg)](https://www.python.org/downloads/release/python-390/)
[![Python 3.10](https://img.shields.io/badge/python-3.10-blue.svg)](https://www.python.org/downloads/release/python-3100/)

## Usage
### install
    git clone git@github.com:code-127/luhn-formula.git
### Example
    >>> from luhnformula import luhnformula as lf
    >>> lf.getcheckdigit("12345")
    '5'
    >>> lf.addcheckdigit("12345")
    '123455'
    >>> lf.isvalid("123455")
    True
## Function
### isvalid(number: str) -> bool:
    Validate number with the Luhn formula.
    Args:
        number: Number to validate.
    Returns:
        ``True`` when the: number is valid, otherwise ``False``.
### getcheckdigit(number: str) -> str:
    Generate check digit with the Luhn formula for a number.
    Args:
        number: Number used to generate the check digit.
    Return:
        the check digit for a number.
    Raise error:
        ValueError : Invalid number.
### addcheckdigit(number: str) -> str:
    Generate and add check digit with the luhn formula for a number
    Args:
        number: Number used to generate the check digit.
    Return:
        the number with the check digit.
    Raise error:
        ValueError : Invalid number.
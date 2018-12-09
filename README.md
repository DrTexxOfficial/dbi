| BRANCH  | BUILD STATUS | COVERAGE | ISSUES | OPEN PRs |
| ---     | :---:        | :---:    | :---:  | :---:    |
| Master  | [![Build Status](https://travis-ci.org/DrTexxOfficial/dbi.svg?branch=master)](https://travis-ci.org/DrTexxOfficial/dbi) | [![codecov](https://codecov.io/gh/DrTexxOfficial/dbi/branch/master/graph/badge.svg)](https://codecov.io/gh/DrTexxOfficial/dbi) | [![GitHub issues](https://img.shields.io/github/issues/DrTexxOfficial/dbi.svg?branch=master)](https://GitHub.com/DrTexxOfficial/dbi/issues/) | [![GitHub pull-requests](https://img.shields.io/github/issues-pr/DrTexxOfficial/dbi.svg?branch=master)](https://GitHub.com/DrTexxOfficial/dbi/pull/) |
| Develop | [![Build Status](https://travis-ci.org/DrTexxOfficial/dbi.svg?branch=develop)](https://travis-ci.org/DrTexxOfficial/dbi) | [![codecov](https://codecov.io/gh/DrTexxOfficial/dbi/branch/develop/graph/badge.svg)](https://codecov.io/gh/DrTexxOfficial/dbi) |

# Debug Interface - DBI 

[![PyPI Version](https://img.shields.io/pypi/v/dbi.svg)](https://pypi.python.org/pypi/dbi/)
[![GitHub release](https://img.shields.io/github/release/drtexxofficial/dbi.svg)](https://GitHub.com/DrTexxOfficial/dbi/releases/)
[![GitHub license](https://img.shields.io/github/license/DrTexxOfficial/dbi.svg?branch=master)](https://github.com/DrTexxOfficial/dbi/blob/master/LICENSE)
[![Github all releases](https://img.shields.io/github/downloads/DrTexxOfficial/dbi/total.svg)](https://GitHub.com/DrTexxOfficial/dbi/releases/)

<img src="docs/dbi_logo.png" alt="dbi logo" width="200"/>

## Installation
### Install via pip
Install as user (recommended):

    $ pip3 install dbi --user

Install as root:

    $ sudo pip3 install dbi

### Install from source
Clone this repository:

    $ git clone https://github.com/DrTexxOfficial/dbi.git

Install requirements:

    $ cd dbi
    $ pip3 install -r requirements.txt --user
    
## Script Functionality
### User-Written Verbosity-Dependant Debug Messages
- information is only show when A and B are satisfied
    - debugging is active
    - the threshold verbosity is reached or exceeded (this threshold is specified on a per-message basis)
- verbosity can be
    - set in advanced
    - **modified on-the-fly**
- multiple **external functions** can be executed in a single-line
- users can write their own debugging messages on the status of each function's progress
- console output is colour-coded (based on verbosity levels)

## What is the purpose?
My console had become populated by indecernable walls of debugging text, all thanks to riddling my scripts with lines like `print(str(var),var)` for debugging.
So I created a module to maintain my sanity and save my time.

## Examples
Initial config:
```python3
from dbi import Dbi
dbi = Dbi(3,True)
dpm = dbi.print_message
```
Generic example:
```
[IN ]: dpm(2,"message with","sub-message")
[OUT]: [3][2]<=[2018-12-10 01:54:59.845995] message with | sub-message
```

<br/>

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

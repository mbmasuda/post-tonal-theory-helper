# post-tonal-theory-helper

#### by Mari Masuda <mbmasuda.github@gmail.com>

This package provides some basic post-tonal music theory
analysis functions for Python 3.

Based on the text *Introduction to Post-Tonal Theory*
by Joseph N. Straus (ISBN 0-13-686692-1)


## Installation

```bash
$ pip install post-tonal-theory-helper-mbmasuda
```

## Usage

```python
from ptth.api import *

pitches = '0t38e'

normal = normal_form(pitches)
prime = prime_form(pitches)

normal_t4 = transpose(normal, 4)
normal_t4i = invert(normal, transpose=4)

boolean1 = is_transpositionally_related(normal, normal_t4)
boolean2 = is_inversionally_related(normal, normal_t4i)

members = get_set_class_members(normal)

forte_name = get_forte_name(pitches)
```

## Tests

Tests can be run with pytest

```bash
$ py.test
```

## TODO

1.  **Clean up the code**

    I threw this package together pretty quickly because the point of this
    project was to learn how to publish something to PyPI. Although the
    code works fine and there are tests, I need to fix some stuff up because
    some of the docstrings are out of sync with the code and also I noticed
    a few PEP-8 issues as well

# SublimePythonAndDjangoHelpers

Sublime Text 3 Python and Django helpers. Very basic at this time, but it will probably grow over time.


## Snippets

The snippets are used as follows:

- Type the name of the snippet (as listed below), and hit TAB.
- You can autocomplete snippets with CTRL-SPACE, so you should only have to
  type a few characters of the snippet.


### get_context_data
Create the ``get_context_data(..)`` method of django class based template views. Expands to:

```python
def get_context_data(self, **kwargs):
	context = super(${1:ClassName}, self).get_context_data(**kwargs)
    context['${2:contextvariable}'] = ${3:value}
    return context
```


### pprint
Expands to:

```python
from pprint import pprint
pprint(${1})
```

Great for debugging.


### blockprint
Expands to:

```python
print
print
print '='*70
print
print ${1}
print
print '='*70
print
print
```

Great for debugging print within verbose output.


### import_reverse
Expands to:
```python
from django.core.urlresolvers import reverse
```


### TemplateView
Expands to:

```python
from django.views.generic import TemplateView

class ${1:MyView}(TemplateView):
    template_name = '${2}'
```


### TestCase
Expands to:

```python
from django.test import TestCase

class Test${1:Something}(TestCase):
    def setUp(self):
        ${2:pass}

    def test_${3:something}(self):
        ${4}
```

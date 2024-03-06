deprecated_params
=================

-  This library provides a decorator deprecated_params that allows you
   to deprecate certain parameters in your class methods or function.



.. image:: https://img.shields.io/pypi/v/pdeprecator
   :target: https://pypi.python.org/pypi/pdeprecator/

.. image:: https://github.com/Agent-Hellboy/pdeprecator/actions/workflows/python-app.yml/badge.svg
    :target: https://github.com/Agent-Hellboy/pdeprecator/
    
.. image:: https://img.shields.io/pypi/pyversions/pdeprecator.svg
   :target: https://pypi.python.org/pypi/pdeprecator/

.. image:: https://img.shields.io/pypi/l/pdeprecator.svg
   :target: https://pypi.python.org/pypi/pdeprecator/

.. image:: https://pepy.tech/badge/pdeprecator
   :target: https://pepy.tech/project/pdeprecator

.. image:: https://img.shields.io/pypi/format/pdeprecator.svg
   :target: https://pypi.python.org/pypi/pdeprecator/

.. image:: https://coveralls.io/repos/github/Agent-Hellboy/pdeprecator/badge.svg?branch=master
   :target: https://coveralls.io/github/Agent-Hellboy/pdeprecator?branch=master

Installation
------------

For stable version 
   - pip install pdeprector

For developement 
   - git clone https://github.com/Agent-Hellboy/pdeprector
   - cd pdeprector 
   - python -m venv .venv 
   - source .venv/bin/activate

Example
-------

.. code:: python

   # Example usage
   class MyClass:
       @deprecated_params({"old_param": "new_param"})
       def __init__(self, new_param):
           self.new_param = new_param


   # Usage
   obj = MyClass(old_param="value")
   print(obj.new_param)

Warning
-------

::

   - It's recommended to write new functions or classes with a v2 suffix instead of using this deprecated library. 

   - If possible, migrate to the newer version with v2 suffix.    
     
     However, if migration is not feasible at the moment, you can continue using this library with caution.

   You should do following 

.. code:: python

     pip install deprecated

     from deprecated import deprecated

     # Deprecate a function
     @deprecated(reason="Use another_function instead")
     def deprecated_function():
         pass

     # Deprecate a class method
     class MyClass:
         @deprecated(reason="Use another_method instead")
         def deprecated_method(self):
             pass

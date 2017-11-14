.. title: First Theano Example
.. slug: first-theano-example
.. date: 2017-11-12 16:56:09 UTC-08:00
.. tags: 
.. category: theano
.. link: 
.. description: A test of theano
.. type: text

`Theano <http://deeplearning.net/software/theano/index.html>`_ is a python library for evaluating mathematical expressions.

1 Imports
---------

.. code:: ipython

    import theano
    from theano import tensor

2 Some values
-------------

.. code:: ipython

    a = tensor.dscalar()
    b = tensor.dscalar()
    c = a + b

At this point 'c' is a symbolic expression without any concrete value, it just knows you are going to add two numbers (scalars).

3 Expression to function
------------------------

So now we make into a callable function.

.. code:: ipython

    c_function = theano.function([a,b], c)

4 Pass in some values
---------------------

And then pass in some values for it to evaluate.

.. code:: ipython

    print(c_function(5.0, 1.6))

::

    6.6

5 Conclusion
------------

This shows how you can create a simple equation and evaluate it with concrete values using theano. In this case we used scalar values, but as the name (\`\`tensor\`\`) suggests, it is oriented toward vector calculations.

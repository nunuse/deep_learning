.. title: First TensorFlow Example
.. slug: first-tensorflow-example
.. date: 2017-11-13 12:33:35 UTC-08:00
.. tags: tensorflow
.. category: 
.. link: 
.. description: A first tensorflow example.
.. type: text

`Tensor Flow <https://www.tensorflow.org>`_ is a library for numerical computation that uses data-flow graphs. The data that flows between the nodes in the graph are represented as tensors, thus the name.

1 Imports
---------

.. code:: ipython

    import tensorflow

2 Declaring Some Variables
--------------------------

.. code:: ipython

    a = tensorflow.placeholder(tensorflow.float32)
    b = tensorflow.placeholder(tensorflow.float32)

3 An Add Function
-----------------

.. code:: ipython

    adder = tensorflow.add(a, b)

4 Bind Some Data to the Variables
---------------------------------

.. code:: ipython

    binding = {a: 2.3, b: 6.6}

5 Run the Session
-----------------

.. code:: ipython

    session = tensorflow.Session()
    print(session.run(adder, feed_dict=binding))

::

    8.9

Runtime Performance Comparison
==============================

Because sortedcontainers is implemented in pure-Python, its performance depends
directly on the Python runtime. SortedContainers was primarily developed, tested
and benchmarked on CPython 2.7, specifically build:

::

    Python 2.7.8 (default, Jul 13 2014, 17:11:32) 
    [GCC 4.2.1 Compatible Apple LLVM 5.1 (clang-503.0.40)] on darwin

Not all runtimes are created equal. The graphs below compare sortedcontainers
running on the CPython 2.7, CPython 3.4 and PyPy 2.2 runtimes. In general
CPython 3.4 is about half the speed of CPython 2.7. The PyPy 2.2 runtime
displays much more variability due to its JIT-ed nature. Once the just-in-time
compiler optimizes the code, performance is often several to tens of times
faster.

Performance of competing implementations are benchmarked against the CPython 2.7
runtime. An :doc:`implementation performance comparison<performance>` is also
included with data from popular sorted container packages.

SortedList
----------

Graphs comparing :doc:`SortedList<sortedlist>` performance.

add
...

Randomly adding values using :ref:`SortedList.add<SortedList.add>`.

.. image:: _static/SortedList-runtime-add.png

contains
........

Randomly testing membership using :ref:`SortedList.__contains__<SortedList.__contains__>`.

.. image:: _static/SortedList-runtime-contains.png

count
.....

Counting objects at random using :ref:`SortedList.count<SortedList.count>`.

.. image:: _static/SortedList-runtime-count.png

__delitem__
...........

Deleting objects at random using :ref:`SortedList.__delitem__<SortedList.__delitem__>`.

.. image:: _static/SortedList-runtime-delitem.png

__getitem__
...........

Retrieving ojbects by index using :ref:`SortedList.__getitem__<SortedList.__getitem__>`.

.. image:: _static/SortedList-runtime-getitem.png

index
.....

Finding the index of an object using :ref:`SortedList.index<SortedList.index>`.

.. image:: _static/SortedList-runtime-index.png

iter
....

Iterating a SortedList using :ref:`SortedList.__iter__<SortedList.__iter__>`.

.. image:: _static/SortedList-runtime-iter.png

pop
...

Removing the last object using :ref:`SortedList.pop<SortedList.pop>`.

.. image:: _static/SortedList-runtime-pop.png

remove
......

Remove an object at random using :ref:`SortedList.remove<SortedList.remove>`.

.. image:: _static/SortedList-runtime-remove.png

update_large
............

Updating a SortedList with a large iterable using :ref:`SortedList.update<SortedList.update>`.

.. image:: _static/SortedList-runtime-update_large.png

update_small
............

Updating a SortedList with a small iterable using :ref:`SortedList.update<SortedList.update>`.

.. image:: _static/SortedList-runtime-update_small.png

SortedDict
----------

Graphs comparing :doc:`SortedDict<sorteddict>` performance.

__getitem__
...........

Given a key at random, retrieve the value using :ref:`SortedDict.__getitem__<SortedDict.__getitem__>`.

.. image:: _static/SortedDict-runtime-getitem.png

__setitem__
...........

Given a key at random, set the value using :ref:`SortedDict.__setitem__<SortedDict.__setitem__>`.

.. image:: _static/SortedDict-runtime-setitem.png

__delitem__
...........

Given a key at random, delete the value using :ref:`SortedDict.__delitem__<SortedDict.__delitem__>`.

.. image:: _static/SortedDict-runtime-delitem.png

iter
....

Iterate the keys of a SortedDict using :ref:`SortedDict.__iter__<SortedDict.__iter__>`.

.. image:: _static/SortedDict-runtime-iter.png

setitem_existing
................

Given an existing key at random, set the value using :ref:`SortedDict.__setitem__<SortedDict.__setitem__>`.

.. image:: _static/SortedDict-runtime-setitem_existing.png

SortedSet
---------

Graphs comparing :doc:`SortedSet<sortedset>` performance.

add
...

Randomly add values using :ref:`SortedSet.add<SortedSet.add>`.

.. image:: _static/SortedSet-runtime-add.png

contains
........

Randomly test membership using :ref:`SortedSet.__contains__<SortedSet.__contains__>`.

.. image:: _static/SortedSet-runtime-contains.png

difference_large
................

Set difference using :ref:`SortedSet.difference<SortedSet.difference>`.

.. image:: _static/SortedSet-runtime-difference_large.png

difference_medium
.................

Set difference using :ref:`SortedSet.difference<SortedSet.difference>`.

.. image:: _static/SortedSet-runtime-difference_medium.png

difference_small
................

Set difference using :ref:`SortedSet.difference<SortedSet.difference>`.

.. image:: _static/SortedSet-runtime-difference_small.png

difference_tiny
...............

Set difference using :ref:`SortedSet.difference<SortedSet.difference>`.

.. image:: _static/SortedSet-runtime-difference_tiny.png

difference_update_large
.......................

Set difference using :ref:`SortedSet.difference_update<SortedSet.difference_update>`.

.. image:: _static/SortedSet-runtime-difference_update_large.png

difference_update_medium
........................

Set difference using :ref:`SortedSet.difference_update<SortedSet.difference_update>`.

.. image:: _static/SortedSet-runtime-difference_update_medium.png

difference_update_small
.......................

Set difference using :ref:`SortedSet.difference_update<SortedSet.difference_update>`.

.. image:: _static/SortedSet-runtime-difference_update_small.png

difference_update_tiny
......................

Set difference using :ref:`SortedSet.difference_update<SortedSet.difference_update>`.

.. image:: _static/SortedSet-runtime-difference_update_tiny.png

intersection_large
..................

Set intersection using :ref:`SortedSet.intersection<SortedSet.intersection>`.

.. image:: _static/SortedSet-runtime-intersection_large.png

intersection_medium
...................

Set intersection using :ref:`SortedSet.intersection<SortedSet.intersection>`.

.. image:: _static/SortedSet-runtime-intersection_medium.png

intersection_small
..................

Set intersection using :ref:`SortedSet.intersection<SortedSet.intersection>`.

.. image:: _static/SortedSet-runtime-intersection_small.png

intersection_tiny
.................

Set intersection using :ref:`SortedSet.intersection<SortedSet.intersection>`.

.. image:: _static/SortedSet-runtime-intersection_tiny.png

intersection_update_large
.........................

Set intersection using :ref:`SortedSet.intersection_update<SortedSet.intersection_update>`.

.. image:: _static/SortedSet-runtime-intersection_update_large.png

intersection_update_medium
..........................

Set intersection using :ref:`SortedSet.intersection_update<SortedSet.intersection_update>`.

.. image:: _static/SortedSet-runtime-intersection_update_medium.png

intersection_update_small
.........................

Set intersection using :ref:`SortedSet.intersection_update<SortedSet.intersection_update>`.

.. image:: _static/SortedSet-runtime-intersection_update_small.png

intersection_update_tiny
........................

Set intersection using :ref:`SortedSet.intersection_update<SortedSet.intersection_update>`.

.. image:: _static/SortedSet-runtime-intersection_update_tiny.png

iter
....

Iterating a set using :ref:`iter(SortedSet)<SortedSet.__iter__>`.

.. image:: _static/SortedSet-runtime-iter.png

pop
...

Remove the last item in a set using :ref:`SortedSet.pop<SortedSet.pop>`.

.. image:: _static/SortedSet-runtime-pop.png

remove
......

Remove an item at random using :ref:`SortedSet.remove<SortedSet.remove>`.

.. image:: _static/SortedSet-runtime-remove.png

union_large
...........

Set union using :ref:`SortedSet.union<SortedSet.union>`.

.. image:: _static/SortedSet-runtime-union_large.png

union_medium
............

Set union using :ref:`SortedSet.union<SortedSet.union>`.

.. image:: _static/SortedSet-runtime-union_medium.png

union_small
...........

Set union using :ref:`SortedSet.union<SortedSet.union>`.

.. image:: _static/SortedSet-runtime-union_small.png

union_tiny
..........

Set union using :ref:`SortedSet.union<SortedSet.union>`.

.. image:: _static/SortedSet-runtime-union_tiny.png

update_large
............

Set update using :ref:`SortedSet.update<SortedSet.update>`.

.. image:: _static/SortedSet-runtime-update_large.png

update_medium
.............

Set update using :ref:`SortedSet.update<SortedSet.update>`.

.. image:: _static/SortedSet-runtime-update_medium.png

update_small
............

Set update using :ref:`SortedSet.update<SortedSet.update>`.

.. image:: _static/SortedSet-runtime-update_small.png

update_tiny
...........

Set update using :ref:`SortedSet.update<SortedSet.update>`.

.. image:: _static/SortedSet-runtime-update_tiny.png

symmetric_difference_large
..........................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference<SortedSet.symmetric_difference>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_large.png

symmetric_difference_medium
...........................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference<SortedSet.symmetric_difference>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_medium.png

symmetric_difference_small
..........................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference<SortedSet.symmetric_difference>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_small.png

symmetric_difference_tiny
.........................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference<SortedSet.symmetric_difference>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_tiny.png

symm_diff_update_large
......................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference_update<SortedSet.symmetric_difference_update>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_update_large.png

symm_diff_update_medium
.......................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference_update<SortedSet.symmetric_difference_update>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_update_medium.png

symm_diff_update_small
......................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference_update<SortedSet.symmetric_difference_update>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_update_small.png

symm_diff_update_tiny
.....................

Set symmetric-difference using :ref:`SortedSet.symmetric_difference_update<SortedSet.symmetric_difference_update>`.

.. image:: _static/SortedSet-runtime-symmetric_difference_update_tiny.png
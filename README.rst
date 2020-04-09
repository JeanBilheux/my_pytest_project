# my_pytest_project
Everything I will learn in pytest will be part of this repo.

-----------------------------------------------
Set-up for development in a virtual environment
-----------------------------------------------

1. Checkout the code.

.. code-block:: shell

   $ git clone https://github.com/JeanBilheux/my_pytest_project.git
   $ cd my_pytest_project


2. Create the virtual environment and activate it. The
   ``--system-site-packages`` argument lets it use things installed on
   the system as a whole for compiling mantid

.. code-block:: shell

   $ virtualenv -p $(which python3) --system-site-packages .venv
   $ source .venv/bin/activate

3. Install the requirements for running the code

.. code-block:: shell

   $ pip install -r requirements.txt -r requirements_dev.txt

4. Install the code in ``develop`` mode.

.. code-block:: shell

   $ python setup.py develop

5. Try it out. Start ``python`` and try

.. code-block:: python

   import my_pytest_project

Verify you can run the unit tests:

.. code-block:: shell

   $ python -m pytest tests/unit/new/

6. Be done. Deactivate the virtual environment using

.. code-block:: shell

   $ deactivate

-----------------
Running the tests
-----------------
.. _running_tests:

.. code-block:: shell

   $ python -m pytest tests/unit/new/
   $ python -m pytest tests/integration/new/

.. code-block:: shell

   $ python -m pytest -k test_samplelogs


--------------------------
Building the documentation
--------------------------
.. _building_docs:

The site can be build directly using

.. code-block:: shell

   $ sphinx-build -b html docs/ build/sphinx/html

or

.. code-block:: shell

   $ python setup.py build_sphinx

------------
Contributing
------------

Contributing is done through merge requests of code that you have the permission to add.
See `CONTRIBUTING.rst <CONTRIBUTING.rst>`_ for more information.

Sources:
- **Python Testing with pytest** from Brian Okken

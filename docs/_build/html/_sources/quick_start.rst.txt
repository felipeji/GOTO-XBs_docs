Quick Start Guide
=================


Downloading GOTO-XBs Repository
-------------------------------

The source code for GOTO-XBS is hosted on the GOTO GitHub page. To developing GOTO-XBs locally, you can clone the repository in : https://github.com/GOTO-OBS/goto-xbs.git




.. _virtual-env:

GOTO-XBs Environment
---------------------

GOTO-XBs requires a specific environment with the necessary dependencies to run smoothly. We maintain two options for creating this environment: using Conda or virtualenv


Using Conda
~~~~~~~~~~~

1. **Install Conda**:

   If you haven't already, download and install Conda. We suggest to use Miniconda, a minimal installer for Conda, from the `official Miniconda website <https://docs.conda.io/en/latest/miniconda.html>`_.

2. **Create a Conda Environment**:

   Open your terminal and create a new Conda environment named 'goto-xbs' using ``goto-xbs-env.yml`` file (provided in the root directory):

   .. code-block:: shell

      conda env create -f goto-xbs-env.yml

3. **Activate the Environment**:

   To activate the newly created environment:

   .. code-block:: shell

      conda activate goto-xbs

and you should now be in the 'goto-xbs' environment.



Using virtualenv
~~~~~~~~~~~~~~~~


1. **Install Python**:

   You will need Python 3.8.x installed on your system (check `official Python website <https://www.python.org/downloads/>`_. in case you need it)

2. **Create a virtualenv**:

   Open your terminal and navigate to the root directory of your GOTO-XBs project. Create a virtual environment named 'goto-xbs' using the following command:

   .. code-block:: shell

      python -m venv goto-xbs

3. **Activate the Environment**:

     .. code-block:: shell

        source goto-xbs/bin/activate

   You should now be in the 'goto-xbs' virtual environment.

3. **Installing Dependencies**:

You can now install the project's dependencies using the ``requirements.txt`` file:

.. code-block:: shell

   pip install -r requirements.txt




Your environment is now set up with all the necessary dependencies for GOTO-XBs. You can proceed to run and use the platform.


Settings Files
--------------

Settings are organized into three separate files: ``dev_settings.py``, ``production_settings.py``, and ``base_settings.py``.

- ``dev_settings.py``: is the app settings used when running in a development environment.

- ``production_settings.py``: is employed when deploying the system in a production environment.

- ``base_settings.py``: contains settings common to both the development and production environments. It is loaded at the start of both `dev_settings.py` and `production_settings.py`, reducing redundancy and ensuring consistency.



To switch between development and production settings, you need to define the ``DJANGO_SETTINGS_MODULE`` system variable.

To activate development settings, use the following command in your terminal::

   $ export DJANGO_SETTINGS_MODULE=goto_xbs.dev_settings

To activate production settings, use this command::

   $ export DJANGO_SETTINGS_MODULE=goto_xbs.production_settings


You can verify the current state of the ``DJANGO_SETTINGS_MODULE`` variable echoing in the terminal by::

   $ echo $DJANGO_SETTINGS_MODULE

This will display the currently active settings module.
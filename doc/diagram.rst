.. _diagram:

The BinderHub Architecture
==========================

BinderHub connects several services together to provide on-the-fly creation
and registry of Docker images. After a user inputs a GitHub repo name or URL,
BinderHub primarily does the following things:

1. Builds automatically a Docker container image using
   `Repo2Docker <https://github.com/jupyter/repo2docker>`_.
2. Registers this Docker image with an online registry.
3. Sends registry information to a JupyterHub instance that then serves the
   Docker image.

Here is a high-level overview of the components that make up BinderHub.

.. raw:: html

   <img src="_static/binder_flow.svg" />

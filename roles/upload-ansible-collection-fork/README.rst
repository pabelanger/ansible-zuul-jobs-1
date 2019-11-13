Upload ansible collections to Ansible Galaxy

**Role Variables**

.. zuul:rolevar:: ansible_galaxy_info

   Complex argument which contains the information about the galaxy
   server as well as the authentication information needed. It is
   expected that this argument comes from a `Secret`.

  .. zuul:rolevar:: token

     Password to use to log in to PyPI.

  .. zuul:rolevar:: url
     :default: The built-in twine default for the production pypi.org service.

     URL of the PyPI repostory.

.. zuul:rolevar:: ansible_galaxy_collection_path 
   :default: {{ ansible_user_dir }}/{{ zuul.project.src_dir }}/*.tar.gz

   Path containing artifacts to upload.

.. zuul:rolevar:: ansible_galaxy_executable
   :default: twine

   Path to ansible-galaxy executable.

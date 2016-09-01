chef-git-hooks
================

githooks(5) scripts to work with repositories of Chef code.


Installation
------------

Just copy the scripts to your repository into the ``.git/hooks/`` directory.
Make sure that the filename conforms to one of the hooks listed in
[githooks(5)](http://git-scm.com/docs/githooks) and that the executable bit
has been set.

If you use submodules:
```
cookbook_target="blau" ; cd ${HOME}/git/chef-repo/.git/modules/cookbooks/${cookbook_target}/hooks/ ; ln -s ${HOME}/git/chef-git-hooks/hooks/pre-commit . ; ln -s ${HOME}/git/chef-git-hooks/hooks/pre-push .
```


Hooks
-----
**pre-commit:**

Check syntax only

**pre-push:**

Do the knife cookbook upload COOKBOOK


Scripts
------

A shell script to check your cookbook before you apply pre-commit scripts

License
-------
Copyright (c) 2016 Roberto Scudeller

This script is licensed under the Apache License, Version 2.0.

See http://www.apache.org/licenses/LICENSE-2.0.html for the full license text.

# turris-os-packages-plugin-template

Packaging template for reForis plugins.

 
## How to
1. Install [cookiecutter](https://cookiecutter.readthedocs.io/en/latest/)
    ```bash
    $ pip3 install cookiecutter
    ```

2. Install template and fill template variables
    ```bash
    $ cookiecutter https://gitlab.labs.nic.cz/turris/reforis/turris-os-packages-plugin-template
    ```
    If `cookiecutter` command is not available try `python3 -m cookiecutter`.

3. Add proper `foris-controller` plugin module to `DEPENDS` variable in `Makefile`.

4. Copy result directory to repository [turris-os-packages](https://gitlab.labs.nic.cz/turris/turris-os-packages/tree/master/web/reforis)
into `web/reforis` directory.

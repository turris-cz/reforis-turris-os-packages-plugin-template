# Turris OS Packages Plugin Template

Packaging template for reForis plugins.

## How-To

1. Install [cookiecutter](https://cookiecutter.readthedocs.io/en/latest/)

```bash
pip install cookiecutter
```

2. Install template and fill template variables

```bash
cookiecutter https://gitlab.nic.cz/turris/reforis/turris-os-packages-plugin-template
```

If the `cookiecutter` command is not available try `python3 -m cookiecutter`.

If you want to use template from specific branch e.g. `dev`

```bash
cookiecutter https://gitlab.nic.cz/turris/reforis/turris-os-packages-plugin-template --checkout dev
```

3. Add proper `foris-controller` plugin module to the `DEPENDS` variable in
   `Makefile`.

```makefile
DEPENDS:=\
   +foris-controller-example-module
```

4. Copy the result directory to the repository
   [turris-os-packages](https://gitlab.nic.cz/turris/os/packages/-/tree/master/web/reforis)
   into the `web/reforis` directory.

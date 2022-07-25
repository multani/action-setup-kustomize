# GitHub Action to install Kustomize

This GitHub Action installs a specific version of the [`kustomize` command line
tool](https://kustomize.io/):

```yaml
      - name: Setup Kustomize
        uses: multani/action-setup-kustomize@v1
        with:
          version: 4.0.2

      - run: kustomize version
```


## Usage

```yaml
- name: Install Kustomize
  uses: multani/action-setup-kustomize@v1
```

Then, simply run the `kustomize` command line tool.

By default, it will install one of the latest version.

You can also request a specific version of Kustomize:

```yaml
- name: Install Kustomize
  uses: multani/action-setup-kustomize@v1
  with:
    version: 4.5.4
```


## Inputs

* `version`: the version of Kustomize to install. The version should be an
  available version from the [release
  page](https://github.com/kubernetes-sigs/kustomize/releases).


## Outputs

None.


## Acknowledgements

The code of this action heavily borrows from the [asdf installation script for
Kustomize by Banno](https://github.com/Banno/asdf-kustomize).


## License

MIT

# h3sdk-buildpack

This is a [Cloud Foundry builpack](https://docs.cloudfoundry.org/buildpacks/) that download, untar and copy a tarball containing your app dependencies when building.

## Usage:

Your should provided the following env vars:

- `SDK_URL`: the url where the tarball should be downloaded
- `SDK_TARGET`: the name of the tarball file

Here is a manifest file example:

```yaml
applications:
- name: MyAwesomeApp
  manifest:
    buildpack: https://github.com/sicara/h3sdk-buildpack.git
    env:
      SDK_TARGET: 'my_dependencies.tar.gz'
      SDK_URL: 'http://dep.toto.fr
```

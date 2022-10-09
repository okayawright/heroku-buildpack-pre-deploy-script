# heroku-buildpack-pre-deploy-script

Add support for pre-deployment scripted tasks.

## Usage

This buildpack works best with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) so that it can be used with your app's existing buildpacks.

After building and before deployment, execute a shell script named `PREDEPLOY`.

## Example

#### .buildpacks

    https://github.com/okayawright/heroku-buildpack-pre-deploy-script

#### PREDEPLOY

    #!/bin/sh
    mkdir -p bin/assets
    cp -Rf assets/* bin/assets/

## License

MIT

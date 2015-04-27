# heroku-buildpack-apt

Add support for apt-based dependencies during both compile and runtime.

## Usage

This buildpack works best with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) so that it can be used with your app's existing buildpacks.

Include a list of apt package names to be installed in a file named `Aptfile`

## Example

#### .buildpacks

    https://github.com/ddollar/heroku-buildpack-apt
    https://github.com/heroku/heroku-buildpack-ruby

#### Aptfile

    libc-i386
    jq

### Check out the PG library version

    $ heroku run "jq -V"
    ~ $ jq version 1.3
	
## License

MIT

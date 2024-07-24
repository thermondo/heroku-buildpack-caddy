# Heroku Caddy Buildpack

Run [Caddy](https://caddyserver.com/) in Heroku.

Built according to Heroku's [buildpack API](https://devcenter.heroku.com/articles/buildpack-api).

## Quick Start

Add the buildpack to your Heroku app:

```bash
heroku buildpacks:add https://github.com/thermondo/heroku-buildpack-caddy/releases/download/v0.0.1/buildpack.tar.gz
```

🚨 _It's highly recommended that you use the **release tarball** URL instead of the GitHub repo URL._

Then in your app's [Procfile](https://devcenter.heroku.com/articles/procfile) add something like this:

```plaintext
web: ./caddy/bin/caddy --config <your Caddyfile>
```

If you want to run a specific version of Caddy, set the `CADDY_RELEASE` environment variable on your
app as seen on [Caddy's GitHub releases](https://github.com/caddyserver/caddy/releases) (for
example: `v2.8.4`). Otherwise it will install the latest version of Caddy from GitHub.

## Developing

### Creating Releases

Go to [the release workflow](https://github.com/thermondo/heroku-buildpack-caddy/actions/workflows/release.yml)
and manually trigger a release. Specify an appropriate tag name using semantic versioning rules.

Then go to the newly created draft release on the [releases page](https://github.com/thermondo/heroku-buildpack-caddy/releases),
polish it up, and publish it.

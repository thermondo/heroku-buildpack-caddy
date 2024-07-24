# Heroku Caddy Buildpack

Run [Caddy](https://caddyserver.com/) in Heroku.

<https://devcenter.heroku.com/articles/buildpack-api>

The Caddy executable will be installed under the `/caddy/bin` directory in your application root.

If you want to run a specific version of Caddy, set the `CADDY_RELEASE` environment variable as
seen on [GitHub releases](https://github.com/caddyserver/caddy/releases) (for example: `v2.8.4`).
Otherwise it will download the latest from GitHub.

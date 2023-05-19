# Libreddit

The docker compose file is intended to start libreddit along with caddy for
serving libreddit over https. So, first generate a pair of SSL certificates; you can use `mkcert`
utility:

```sh
cd certs

# mkcert domain_name
# e.g.
mkcert l.ib
```

This will generate a pair of private and public certificates like `l.ib-key.pem`
and `l.ib.pem`. Ensure that these certificates are placed under the `certs`
directory.

In `Caddyfile`, replace the domain `.l.ib` with your preferred domain.

Finally, start the docker containers:
```sh
docker compose up -d
```

Visit the libreddit instance at: https://l.ib (or https://domain_name)

# javohir-hoshimov.uz

Personal site — static HTML/CSS, no build step.

Live at [javohir-hoshimov.uz](https://javohir-hoshimov.uz), served by nginx from
`/root/javohir-hoshimov` on the host aliased `myserv`.

## Pages

One page, `index.html` at `/`. Project thumbnails live in `img/`.

`experience.html`, `projects.html`, `stack.html` and `contact.html` are redirect
stubs to the matching `/#section`, kept so old links keep working.

nginx resolves extensionless URLs via `try_files $uri $uri/ $uri.html`.

## Deploy

The server holds a clone of this repo, so deploying is a pull:

```sh
ssh myserv 'cd /root/javohir-hoshimov && git pull'
```

Static files only — no nginx reload needed.

# Ident Archive

Ident archive is an archive of TV ads, intros, idents, etc.

It is built with [Jekyll](https://jekyllrb.com/).

Contributions are more than welcome! Please read the [contribution guidelines](CONTRIBUTING.md) before submitting a pull request.

## Start server

The first time you start the server you have to run the following commands:

```bash
bundle install
```

The built-in Jekyll server can't handle this amount of video files. Because of this you have to run the following two commands in two different windows:

```bash
bundle exec jekyll build --watch
bundle exec thin start -p 4000
```

This will build the site and start a webserver on port 4000. You can now access the site at http://localhost:4000.

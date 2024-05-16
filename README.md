# NetFabric Webpage

## Serve locally

After installing Jekyll:

```sh
jekyll serve --livereload
```

Using docker:

```sh
docker run --rm -it -e JEKYLL_ROOTLESS=1 -v "$(pwd):/srv/jekyll" -p 4000:4000 jekyll/jekyll jekyll serve --livereload --host 0.0.0.0
```

## Build webpage

```sh
docker run --rm -it -e JEKYLL_ROOTLESS=1 -v "$(pwd):/srv/jekyll" -p 4000:4000 jekyll/jekyll jekyll build
rm -f netfabric_site.zip
zip -r netfabric_site.zip _site
```

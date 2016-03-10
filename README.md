# How to publish a static website?

## On GitHub Pages

1. Create and switch to `gh-pages` branch: `git checkout -b gh-pages`
2. Add `index.html` and other source files for your website.
3. Create `.nojekyll` file.
4. Create `CNAME` if you want to setup your own domain. Add your domain name to `CNAME` file, e.g.: `artemij.com`
5. Commit: `git commit -m "Add files"`
6. Push: `git push --set-upstream origin gh-pages`

### With your custom domain

1. Log in to your domain provides, e.g. NameCheap, GoDaddy, etc.
2. Select domain name and edit it's DNS settings.
3. Add `A` type record:
  + Host: `@`
  + Points to: `192.30.252.153`
  + TTL: `600` seconds or similar
4. Add `A` type record:
  + Host: `@`
  + Points to: `192.30.252.154`
  + TTL: `600` seconds or similar
5. Save.

Learn more: https://help.github.com/articles/setting-up-an-apex-domain/#configuring-a-records-with-your-dns-provider

## On Surge
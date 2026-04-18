# The Sanctum Method

Source repository for [odehamik.github.io/sanctum-method](https://odehamik.github.io/sanctum-method).

The site is built with [Quartz v4](https://quartz.jzhao.xyz). Content lives in `content/` as plain markdown files. On every push to `main`, a GitHub Action rebuilds the site and deploys it to GitHub Pages.

## Updating the site

Edit any markdown file in `content/`, then from this folder run:

```
bash push "short note on what changed"
```

The script stages everything, commits with your message, and pushes. The Action handles the rest. Site is live within a minute or two.

(If you ever want the shorter `./push "msg"` form, run `chmod +x push` once in your own Terminal and it'll stick.)

## Local preview

To see changes before pushing:

```
npx quartz build --serve
```

Serves at `http://localhost:8080`.

# A set of GitHub pages describing the status of various Qualcomm platforms.

## Testing it locally

- Install Ruby and bundler:

  ```bash
  sudo apt install bundler
  ```

- Setup bundler to use user path for all the storage:

  ```bash
  bundle config set --local path ~/.local/lib/
  ```

- Install all the dependencies:

  ```bash
  bundle install
  ```

- Just rebuild the data:
  ```
  ./regen.py
  bundle exec jekyll build
  ```
  Now you can check the HTML data built in `./_site/`.

- Or execute a local Jekyll server, providing an ongoing preview:

  ```bash
  bundle exec jekyll serve
  ```

  Now you can open [localhost:4000](http://127.0.0.1:4000/msm/) with your Web
  browser. Jekyll will automatically regenerate the pages if any of the source
  files changes.

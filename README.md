# Modified Readme - original at the repo (github.com/tripit/slate)

## Running this locally
1. Download the repo, of course
2. Install RVM (very much like `virtualenv`) for python. [Steps here](https://rvm.io/rvm/install)
3. Install Ruby using RVM. I am using [ruby-2.2.0](https://www.ruby-lang.org/en/news/2014/12/25/ruby-2-2-0-released/)
4. Install bundler gem `gem install bundler`
5. Run the test server using `bundle exec middleman server`

## Making Changes
1. Folder `source/includes` has the actual Markdown files
2. These markdown files are referenced in the TOC in `source/index.md`
```
includes:
  - authentication
  - userdetails
```
    In the example above, `_authentication.md` in the `source/includes` directory is automatically found and used
3. Title (on the side bar) is the same as the title of `_authentication.md`
4. Source goes first in the `_authentication.md`, source is shown on the right side
5. Notes to be shown go at the very end
6. Tables are supported

## Next Steps
* Go forth and conquer

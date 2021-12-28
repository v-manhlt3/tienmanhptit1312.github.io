# Technical Portfolio

This repository hosts a technical portfolio built using [TechFolio](http://techfolios.github.io).

See the quick start guide for instructions on how to tailor the template to your own needs.

Note these directions:

  * https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll

Here was what I did:


```
sudo gem install bundler -n /usr/local/bin
bundle install
bundle exec jekyll serve
```

## Locale problems

If you get the following error:

```
$ bundle exec jekyll serve --baseurl ''
Configuration file: /Users/philipjohnson/github/philipmjohnson/philipmjohnson.github.io/_config.yml
            Source: /Users/philipjohnson/github/philipmjohnson/philipmjohnson.github.io
       Destination: /Users/philipjohnson/github/philipmjohnson/philipmjohnson.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
  Conversion error: Jekyll::Converters::Scss encountered an error while converting 'assets/css/style.scss':
                    Invalid US-ASCII character "\xE2" on line 5
jekyll 3.7.4 | Error:  Invalid US-ASCII character "\xE2" on line 5
```

The solution is to set LANG and LANGUAGE to "utf-8". (Not UTF-8 or en_US.UTF-8.)

An easy way to do this is with this script:

```
$ source set-locale.sh
```


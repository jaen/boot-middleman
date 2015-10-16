# Boot + Middleman

Builds a middleman project from a subdirectory. By default, assumes the
`assets` folder, but this can be configured.

A minimal middleman project will have the following structure:

    assets/
    |-- Gemfile
    |-- config.rb
    `-- source/
        |-- favicon.ico
        |-- index.html.erb
        |-- images/
        |-- javascripts/
        |-- layouts/
        `-- stylesheets/

See the [middleman docs](https://middlemanapp.com/basics/directory-structure/)
for more information.

**NOTE**: Known to work with middleman 3.3.x and 3.4.x


## Setup

In your `build.boot`:

``` clojure
(set-env!
 :resource-paths #{"resources"}
 :dependencies '[[org.clojure/clojure "1.7.0" :scope "provided"]
                 [com.joshuadavey/boot-middleman "0.0.5" :scope "test"]])

(require '[com.joshuadavey.boot-middleman :refer [middleman]])
```

## Usage

```
boot middleman
```

Or, for continuous builds:

```
boot watch middleman
```

For more options, see help with `boot middleman -h`.

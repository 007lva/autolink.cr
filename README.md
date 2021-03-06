# :link: Autolink [![Build Status](https://travis-ci.org/crystal-community/autolink.cr.svg?branch=master)](https://travis-ci.org/crystal-community/autolink.cr)

*Autolink.cr* is a Crystal shard that automatically turns URLs into links.

Example:

```crystal
auto_link("Welcome to my profile https://github.com/hugoabonizio")
# => Welcome to my profile <a href="https://github.com/hugoabonizio">https://github.com/hugoabonizio</a>
```

## Installation

Add this to your application's `shard.yml`:

```yaml
dependencies:
  autolink:
    github: crystal-community/autolink.cr
```

## Usage

```crystal
require "autolink"

include Autolink

auto_link("My blog: http://www.myblog.com/", html: {"class" => "menu", "target" => "_blank"})
# => My blog: <a href="http://www.myblog.com/" class="menu" target="_blank">http://www.myblog.com/</a>
```

### Simple autolink

Without providing any HTML options *autolink.cr* will just wrap the URL with ```<a>``` tag.

```crystal
Autolink.auto_link("Welcome to my new blog at http://www.myblog.com/")
# => Welcome to my new blog at <a href="http://www.myblog.com/">http://www.myblog.com/</a>
```

### Custom tag attributes

The ```<a>``` tag can receive custom attributes.

```crystal
Autolink.auto_link("My blog: http://www.myblog.com/", html: {"class" => "menu", "target" => "_blank"})
# => My blog: <a href="http://www.myblog.com/" class="menu" target="_blank">http://www.myblog.com/</a>
```

## Contributing

1. Fork it ( https://github.com/crystal-community/autolink.cr/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [hugoabonizio](https://github.com/hugoabonizio) Hugo Abonizio
- [veelenga](https://github.com/veelenga) V. Elenhaupt

This project is a port to Crystal of [rails_autolink](https://github.com/tenderlove/rails_autolink) Ruby gem. Thanks to all its [contributors](https://github.com/tenderlove/rails_autolink/graphs/contributors).
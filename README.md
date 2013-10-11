# compass-extensions-sample

Basic Compass project with sample .scss files to demonstrate the usage of [CSS Lint](http://comcast.github.io/compass-csslint/) & [csscss](https://github.com/Comcast/compass-csscss)

## Installation

There is currently a [bug in Compass](https://github.com/chriseppstein/compass/issues/1053) that prevents external Compass commands from being registered if they're required in a project's config.rb file. So until that is resolved, you'll have to build this [custom version of Compass](https://github.com/Comcast/compass/tree/command_extensions) that [adds support for command-line extensions](https://github.com/chriseppstein/compass/pull/1261):

https://github.com/Comcast/compass

Clone that project, then from the project root run

    $ git checkout command_extensions
    $ gem build compass.gemspec

Be sure to take note of the .gem filename

Once that builds, install your locally-built version of Compass

    $ gem install compass-0.13.alpha.4.<hash>.gem

Be sure to use the actual filename that the build command created.

Then, to install additional dependencies execute:

    $ bundle install

## CSS Lint Usage

Run the following command from the root of your Compass project:

    $ compass csslint

To view options:

    $ compass csslint --help

## csscss Usage

Run the following command from the root of your Compass project:

    $ compass csscss

To view options:

    $ compass csscss --help
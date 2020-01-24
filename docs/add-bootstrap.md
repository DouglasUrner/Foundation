## Adding Bootstrap

### With Bootstrap 4

Using Adrian Teh's approach from [Ruby on Rails 6 with Webpacker and Bootstrap][teh], including support for emitting separate CSS files for the `stylesheet_pack_tag` helper.

It appears that once you enable emitting separate CSS, you must use the `stylesheet_pack_tag` helper to include CSS that is managed by Webpack.

It also appears that each stylesheet that you want to pick up from `app/assets/stylesheets` has to be listed individually in `app/javascript/stylesheets/application.scss`.

#### Using MD Bootstrap

### [TailwindCSS](https://tailwindcss.com)

A less "opinionated" alternative to Bootstrap.

#### References

* [How to install TailwindCSS 1.0 with Rails 6+](https://gorails.com/episodes/tailwindcss-1-0-with-rails-6) (April 2019) - Comments suggest that the process in the video may not be entirely debugged.
* [IcaliaLabs/tailwindcss-rails](https://github.com/IcaliaLabs/tailwindcss-rails)
* [justalever/kickoff_tailwind](https://github.com/justalever/kickoff_tailwind)
* [Re-create Airbnb's Home Page with Tailwind CSS](https://www.youtube.com/watch?v=7phZqghhho0) (Oct 2019)

### [Bootstrap 4](https://getbootstrap.com)

#### With Sprockets

* [bootstrap-rubygem](https://github.com/twbs/bootstrap-rubygem)

#### With Webpack

#### References

* [Ruby on Rails 6 with Webpacker and Bootstrap][teh] (July 2019) - Uses [Webpack][], but keeps the stylesheets in `app/assets/stylesheets`.
The code is available on GitHub at: [AdrianTeh/HelloWorldWebpacker](https://github.com/AdrianTeh/HelloWorldWebpacker), however it assumes you have Postgress for your database and it expects Ruby 2.6.3.
* [How to use Bootstrap with Webpack & Rails](https://gorails.com/episodes/how-to-use-bootstrap-with-webpack-and-rails?utm_source=rubyflow&utm_medium=twitter) (April 2019) - Video with a good discussion in the comments on asset layout and working with Webpack.

[teh]: <https://medium.com/@adrian_teh/ruby-on-rails-6-with-webpacker-and-bootstrap-step-by-step-guide-41b52ef4081f>
[webpack]: <>
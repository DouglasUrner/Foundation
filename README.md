# Foundation: a Rails 6 template project

The **master** branch is the fully configured template, ready to be used as the starting point of a project.

Other branches:
* **rails-new**: The result of `rails new foundation` - you can add components individually by basing a new branch on this branch and then merging the components that you want. A minimal controller and view for `home#index` is included and set as the default route.
* **add-bootstrap**:
* **add-devise**:

## Base Rails App

Create a new Rails app:

`rails new foundation` (branch: **rails-new**)

`rails g controller home`

### home#index

For now, an empty `index` method and a trivial `views/home/index.html.erb` will do the trick:

```ruby
def index
end
```

```html
<h1>Foundation</h1>
```

The home controller gives us just enough to set up and test the other components and a target for Devise.

### navbar

## Styling

### With Bootstrap 4

Using Adrian Teh's approach from [Ruby on Rails 6 with Webpacker and Bootstrap][teh], including support for emitting separate CSS files for the `stylesheet_pack_tag` helper:

`yarn add bootstrap jquery popper.js`

It appears that once you enable emitting separate CSS, you must use the `stylesheet_pack_tag` helper to include CSS that is managed by Webpack.

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

### [Font Awesome](https://fontawesome.com)

## User Accounts

### [Devise](https://github.com/heartcombo/devise)

#### References

* [User Authentication in Rails with Devise](https://www.youtube.com/watch?v=ef11ToOE4N0&list=PLGpsnWFCyASUdxcZl3AMarVRHIr05WKYV&index=12) (May 2015) - add **devise** to an existing Rails app.
* [Codeplace | User Authentication in Ruby on Rails using Devise](https://www.youtube.com/watch?v=ZEk0Jp2dThc&list=PLGpsnWFCyASUdxcZl3AMarVRHIr05WKYV&index=5) (January 2015) - starts from scratch. Adds SMTP method to mailer setup (send e-mail through a Gmail account or a similar service). Uses a **home** controller with an **index** action.
* [Using the Devise Gem to Handle Authentication in a Rails App](https://medium.com/swlh/https-medium-com-melee-santiago-using-devise-gem-to-handle-authentication-in-rails-app-538bbd231dde) (May 2019)
* [imhta/rails_6_devise_example](https://github.com/imhta/rails_6_devise_example)

## Roles

### References

* [Use Enum to Represent User Roles in your Database](https://medium.com/@stacietaylorcima/use-enum-to-represent-user-roles-in-your-database-1cd5424fb311) (March 2018)

## Permissions

* [PeterGate](https://github.com/elorest/petergate)
* [Pundit](https://github.com/varvet/pundit)
* [CanCanCan](https://github.com/CanCanCommunity/cancancan)

### References

* [Architecting a Roles & Permissions System Using Rails, GraphQL & React](https://www.atrium.co/inside-atrium/architecting-roles-permissions/) (August 2019) - Lessons: use a naming convention (premission names should be predictable, affirmative permissions only, bundling premissions into roles makes for a cleaner UI and easier reasoning about permissions - the cost is flexbility (you can't have permissions outside of your role), check authorization at the permission level - not the role level.

## Settings & Preferences

[]()

## Customizing

[How to rename rails controller and model in a project](https://stackoverflow.com/questions/11924124/how-to-rename-rails-controller-and-model-in-a-project)

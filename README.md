# SolidusBlankFrontend

If a solidus gem is added to the Gemfile, it will also include several other gems that you might not want, such as solidus_frontend and solidus_sample.
For example, if it is not enough to just make minor changes and additions to frontend by overriding and defacing, 
it may be more practical to get rid off the provided frontend and implement it within the main app. This may be done by
removing `gem 'solidus'` from the Gemfile and replacing it with manual additions of `solidus_core`, `solidus_api` and `solidus_backend`.

However, some other solidus gems relay on the presence of `Spree::Frontend::Engine` in order to load some views and add helper methods.
One of such is [solidus_auth_devise](https://github.com/solidusio/solidus_auth_devise). This gem, *solidus_blank_frontend*, 
mounts a `Spree::Frontend::Engine` whose only purpose is to be detected by such gems.

## Installation

Add this line to your application's Gemfile:

    gem 'solidus_blank_frontend', github: 'Xpitality/solidus_blank_frontend'
    
Please note that it is best to add it just after the three main solidus gems (`solidus_core`, `solidus_api` and `solidus_backend`)  
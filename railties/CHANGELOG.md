*   `BACKTRACE` environment variable to show unfiltered backtraces for
    test failures.

    Example:

        `BACKTRACE=1 ruby -Itest ...`
        # or with rake
        `BAKCTRACE=1 bin/rake`

    *Yves Senn*

*   Removal of all javascript stuff (gems and files) when generating a new
    application using the `--skip-javascript` option.

    *Robin Dupret*

*   Make the application name snake cased when it contains spaces

    The application name is used to fill the `database.yml` and
    `session_store.rb` files ; previously, if the provided name
    contained whitespaces, it led to unexpected names in these files.

    *Robin Dupret*

*   Added `--model-name` option to `ScaffoldControllerGenerator`.

    *yalab*

*   Expose MiddlewareStack#unshift to environment configuration.

    *Ben Pickles*

*   `rails server` will only extend the logger to output to STDOUT
     in development environment.

    *Richard Schneeman*

*   Don't require passing path to app before options in `rails new`
    and `rails plugin new`

    *Piotr Sarnacki*

*   rake notes now searches *.less files

    *Josh Crowder*

*   Generate nested route for namespaced controller generated using
    `rails g controller`.
    Fixes #11532.

    Example:

        rails g controller admin/dashboard index

        # Before:
        get "dashboard/index"

        # After:
        namespace :admin do
          get "dashboard/index"
        end

    *Prathamesh Sonpatki*

*   Fix the event name of action_dispatch requests.

    *Rafael Mendonça França*

*   Make `config.log_level` work with custom loggers.

    *Max Shytikov*

*   Changed stylesheet load order in the stylesheet manifest generator.
    Fixes #11639.

    *Pawel Janiak*

*   Added generated unit test for generator generator using new
    `test:generators` rake task.

    *Josef Šimánek*

*   Removed `update:application_controller` rake task.

    *Josef Šimánek*

*   Fix `rake environment` to do not eager load modules

    *Paul Nikitochkin*

*   Fix `rake notes` to look into `*.sass` files

    *Yuri Artemev*

*   Removed deprecated `Rails.application.railties.engines`.

    *Arun Agrawal*

*   Removed deprecated threadsafe! from Rails Config.

    *Paul Nikitochkin*

*   Remove deprecated `ActiveRecord::Generators::ActiveModel#update_attributes` in
    favor of `ActiveRecord::Generators::ActiveModel#update`

    *Vipul A M*

*   Remove deprecated `config.whiny_nils` option

    *Vipul A M*

*   Rename `commands/plugin_new.rb` to `commands/plugin.rb` and fix references

    *Richard Schneeman*

*   Fix `rails plugin --help` command.

    *Richard Schneeman*

*   Omit turbolinks configuration completely on skip_javascript generator option.

    *Nikita Fedyashev*

*   Removed deprecated rake tasks for running tests: `rake test:uncommitted` and
    `rake test:recent`.

    *John Wang*

*   Clearing autoloaded constants triggers routes reloading.
    Fixes #10685.

    *Xavier Noria*

*   Fixes bug with scaffold generator with `--assets=false --resource-route=false`.
    Fixes #9525.

    *Arun Agrawal*

*   Rails::Railtie no longer forces the Rails::Configurable module on everything
    that subclasses it. Instead, the methods from Rails::Configurable have been
    moved to class methods in Railtie and the Railtie has been made abstract.

    *John Wang*

*   Changes repetitive th tags to use colspan attribute in `index.html.erb` template.

    *Sıtkı Bağdat*

Please check [4-0-stable](https://github.com/rails/rails/blob/4-0-stable/railties/CHANGELOG.md) for previous changes.

In your project, do the following thing:

    git submodule add git@github.com:caillou/vagrant-config-module.git .puppet/modules/nelmio

Now, if you want to disable caching in apache, add the following to your `default.pp` file:

    apache::module {
      'headers':
        templatefile => 'nelmio/apache-mod-headers.conf.erb'
    }

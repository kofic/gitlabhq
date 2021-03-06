## GitLab: self hosted Git management software

![logo](https://raw.github.com/gitlabhq/gitlabhq/master/public/gitlab_logo.png)

### GitLab allows you to
 * keep your code secure on your own server
 * manage repositories, users and access permissions
 * communicate through issues, line-comments and wiki pages
 * perform code review with merge requests

### GitLab is

* powered by Ruby on Rails
* completely free and open source (MIT license)
* used by more than 10.000 organizations to keep their code secure

### Code status

* [![build status](http://ci.gitlab.org/projects/1/status.png?ref=master)](http://ci.gitlab.org/projects/1?ref=master) ci.gitlab.org (master branch)

* [![build status](https://secure.travis-ci.org/gitlabhq/gitlabhq.png)](https://travis-ci.org/gitlabhq/gitlabhq) travis-ci.org (master branch)

* [![Code Climate](https://codeclimate.com/github/gitlabhq/gitlabhq.png)](https://codeclimate.com/github/gitlabhq/gitlabhq)

* [![Dependency Status](https://gemnasium.com/gitlabhq/gitlabhq.png)](https://gemnasium.com/gitlabhq/gitlabhq)

* [![Coverage Status](https://coveralls.io/repos/gitlabhq/gitlabhq/badge.png?branch=master)](https://coveralls.io/r/gitlabhq/gitlabhq)

### Resources

* GitLab.org community site: [Homepage](http://gitlab.org) [Screenshots](http://gitlab.org/screenshots/) [Blog](http://blog.gitlab.org/) [Demo](http://demo.gitlabhq.com/users/sign_in)

* GitLab.com commercial services: [Homepage](http://www.gitlab.com/) [Subscription](http://www.gitlab.com/subscription/) [Consultancy](http://www.gitlab.com/consultancy/) [GitLab Cloud](http://www.gitlab.com/cloud/) [Blog](http://blog.gitlab.com/)

* GitLab CI: [Readme](https://github.com/gitlabhq/gitlab-ci/blob/master/README.md) of the GitLab open-source continuous integration server

### Requirements

* Ubuntu/Debian**
* ruby 1.9.3
* MySQL
* git
* gitlab-shell
* redis

** More details are in the [requirements doc](https://github.com/gitlabhq/gitlabhq/blob/master/doc/install/requirements.md)

### Installation

#### Official production installation

Follow the installation guide for production server.

* [Installation guide for latest stable release (5.0)](https://github.com/gitlabhq/gitlabhq/blob/5-0-stable/doc/install/installation.md) - **Recommended**

* [Installation guide for the current master branch (5.1)](https://github.com/gitlabhq/gitlabhq/blob/master/doc/install/installation.md)


#### Official development installation

If you want to contribute, please first read our [Contributing Guidelines](https://github.com/gitlabhq/gitlabhq/blob/master/CONTRIBUTING.md) and then we suggest you to use the Vagrant virtual machine project to get an environment working with all dependencies.

* [Vagrant virtual machine](https://github.com/gitlabhq/gitlab-vagrant-vm)


#### Unsupported production installation

* [GitLab recipes](https://github.com/gitlabhq/gitlab-recipes) for setup on different platforms

* [Unofficial installation guides](https://github.com/gitlabhq/gitlab-public-wiki/wiki/Unofficial-Installation-Guides)

* [BitNami one-click installers](http://bitnami.com/stack/gitlab)

* [TurnKey Linux virtual appliance](http://www.turnkeylinux.org/gitlab)


### New versions and upgrading

Each month on the 22th a new version is released together with an upgrade guide.

* [Upgrade guides](https://github.com/gitlabhq/gitlabhq/tree/master/doc/update)

* [Changelog](https://github.com/gitlabhq/gitlabhq/blob/master/CHANGELOG)

* Features that will be in the next release are listed on [the feedback and suggestions forum with the status "started"](http://feedback.gitlab.com/forums/176466-general/status/796456).


### Run in production mode

1. The Installation guide contains instructions on how to download an init script and run it automatically on boot. You can also start the init script manually:

        sudo service gitlab start

  or by directly calling the script

        sudo /etc/init.d/gitlab start

### Run in development mode

Start it with [Foreman](https://github.com/ddollar/foreman)

        bundle exec foreman start -p 3000

  or start each component separately

        bundle exec rails s
        bundle exec rake sidekiq:start

### Run the tests

* Seed the database

        bundle exec rake db:setup RAILS_ENV=test
        bundle exec rake db:seed_fu RAILS_ENV=test

* Run all tests

        bundle exec rake gitlab:test

* Rspec unit and functional tests

        bundle exec rake spec

* Spinach integration tests

        bundle exec rake spinach


### GitLab interfaces

* [GitLab API](https://github.com/gitlabhq/gitlabhq/blob/master/doc/api/README.md)

* [Rake tasks](https://github.com/gitlabhq/gitlabhq/tree/master/doc/raketasks)

* [Directory structure](https://github.com/gitlabhq/gitlabhq/blob/master/doc/install/structure.md)

* [Databases](https://github.com/gitlabhq/gitlabhq/blob/master/doc/install/databases.md)


### Getting help

* [Troubleshooting guide](https://github.com/gitlabhq/gitlab-public-wiki/wiki/Trouble-Shooting-Guide) contains solutions to common problems.

* [Support forum](https://groups.google.com/forum/#!forum/gitlabhq) is the best place to ask questions. For example you can use it if you have questions about: permission denied errors, invisible repos, can't clone/pull/push or with web hooks that don't fire. Please search for similar issues before posting your own, there's a good chance somebody else had the same issue you have now and had it resolved. There are a lot of helpful GitLab users there who may be able to help you quickly. If your particular issue turns out to be a bug, it will find its way from there to a fix.

* [Feedback and suggestions forum](http://feedback.gitlab.com) is the place to propose and discuss new features for GitLab.

* [Support subscription](http://www.gitlab.com/subscription/) connect you to the knowledge of GitLab experts that will resolve your issues and answer your questions.

* [Consultancy](http://www.gitlab.com/consultancy/) allows you hire GitLab experts for installations, upgrades and customizations.

* [Contributing guide](https://github.com/gitlabhq/gitlabhq/blob/master/CONTRIBUTING.md) describes how to submit pull requests and issues. Pull requests and issues not in line with the guidelines in this document will be closed.


### Getting in touch

* [Core team](https://github.com/gitlabhq?tab=members)

* [Contributors](https://github.com/gitlabhq/gitlabhq/graphs/contributors)

* [Leader](https://github.com/randx)

* [Contact page](http://gitlab.org/contact/)

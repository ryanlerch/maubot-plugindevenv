# Maubot development environment

## Initial setup

The environment is built around Vagrant:

    $ vagrant up
    $ vagrant ssh


## Add a new client to maubot

A client in maubot is a 1:1 link to a user on matrix.
this returns a link that you have to open in a browser, log in though ipsilon to the
account that will be used on matrix / fedora.im, and it should then be added to maubot

    mbc auth --sso -c -h fedora.im

If you want to use matrix.org and login using a password, run:

    mbc auth -c -h matrix.org


## Setup an instance

Finally go to the webui and login with admin:mypassword and set up an instance
for the plugin to the matrix user:

    http://maubot.tinystage.test:29316/_matrix/maubot/

To use the instance with Tinystage, configure the `maubot-fedora` plugin with:

    fasjson_url: https://fasjson.tinystage.test/fasjson
    pagureio_url: https://pagure.io
    paguredistgit_url: https://src.tinystage.test

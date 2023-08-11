# maubot development environment

    vagrant up
    vagrant ssh
    
    # add a new client to maubot. a client in maubot is a 1:1 link to a user on matrix.
    # this returns a link that you have to open in a browser, log in though ipsilon to the
    # account that will be used on matrix / fedora.im, and it should then be added to maubot
    mbc auth --sso -c -h fedora.im

    # finally go to the webui and login with admin:mypassword and set up an instance 
    # for the plugin to the matrix user

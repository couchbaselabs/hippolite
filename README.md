hippolite

Putting the Hippo CMS on a diet -- by migrating content out of Hippo
to another system as a stepwise, incremental maneuver with no
downtime. In other words, avoid a risky, all-or-nothing, "house moving
day" switch.

The destination system is currently to have a growing set of override
content held as template files in git and to serve those via nginx
which favors those override files and which falls back to proxying to
the upstream https://www.couchbase.com server on any content that
isn't overridden.

Install / dependencies...

For OSX...

    brew install nginx

To start nginx...

    nginx -p . -c nginx.conf

To have nginx reload its nginx.conf file...

    nginx -p . -c nginx.conf -s reload

hippolite

hippolite is either "queen of the amazons", or...

Putting the Hippo CMS on a diet -- by migrating content out of the
Hippo CMS to another system via a stepwise, incremental approach that
avoids downtime. In other words, avoid a risky, all-or-nothing, "house
moving weekend" switch.

The approach is to have nginx serve up local override content files
and also fall back to proxying to the upstream server of
https://www.couchbase.com for any content that's not overridden.

Install / dependencies...

For OSX development...

    brew install nginx

To start nginx...

    nginx -p . -c nginx.conf

To have nginx reload its nginx.conf file...

    nginx -p . -c nginx.conf -s reload

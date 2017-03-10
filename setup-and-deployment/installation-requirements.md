## Installation requirements

We provide compatible Docker containers for production and development with each release of the Livingdocs server and editor. The same goes for elasticsearch and postgresql. We recommend to use the provided Docker setup, but the apps and services can of course also run the classic way. 
 
The following chapters lists the requirements for the Livingdocs editor and server. The Livingdocs editor and Livingdocs server are proprietary software and custom installations require a separate agreement with Livingdocs AG. As an alternative you can consume Livingdocs as a hosted service.


### Editor

The Livingdocs editor consists of static HTML and Javascript files and can in theory be hosted on any static webserver. Our docker setup uses nginx, alternatively you could also deploy it to a cloud service like Amazon S3. The only requirement is currently that the Livingdocs editor needs to run on the root path of a domain, so e.g., `http://yourdomain.com` is fine while `http://yourdomain.com/somepath` would not work.

For custom installations we provide scripts to produce the HTML / CSS / Javascript files that can be uploaded to a host. If you want to write your own installation scripts and your host is publicly accessible, we require that you minify and uglify the Javascript files (you will get an AGB agreement for custom installations that requires this).

The editor uses third party services that are described in the following.

#### Resrc.it

[Resrc.it](https://www.resrc.it/) is used by Livingdocs for 2 things:
- cropping images
- delivering perfectly sized images for different devices
You can create an account on resrc.it and configure it with your image bucket on S3 (see server description).

NOTE: Resrc.it is currently required for a working Livingdocs installation. All image URLs are built by the framework with the assumption that resrc.it is used. There is an experimental support for images without resrc.it that can be enabled in the editor's configuration but is not officially supported.

#### Track.js

This service lets you track Javascript errors and how they happened, i.e., gives you a history of events that led up to an Javascript error in the browser. You can configure your [track.js](https://trackjs.com/) account in the editor's configuration file.

#### Mixpanel (optional)

In order to track your user's usage of Livingdocs you can configure your [mixpanel](https://mixpanel.com/) account in the editor's configuration file.

#### Iframely

IFramely is currently used for 2 things:
- components with automatic metadata fetching from a third-party source (an example of this is the "Teaser" component in our livingdocs-beta.io design)
- automatic validity checks of entered links  
You will need to have an [Iframely](https://iframely.com/) account and configure it with the editor's configuration file.

#### Spellchecker (optional)

Livingdocs supports third-party spellcheckers. You can configure a URL to a spellchecker API in the editor's configuration file. The API specifications are currently not documented, but we're happy to provide this if you need it.

### Server

The server installation is more involved. The server itself is a simple node.js application. Currently, we require a Linux system for the installation (Windows is not supported). The docker container we provide contains all necessary dependencies. You will need to install your own process manager to ensure uptime. We follow the [12 Factor Principles](http://12factor.net/).

Required software on the server are:
- node.js (version 4.x)
- imagemagick (any reasonably new version)

The server depends on the following services and third party services.

#### Postgres

The database of Livingdocs is [Postgres](http://www.postgresql.org/). We support versions 9.3.6 and upwards and the plv8 extension is required.

You will also want to install some kind of backup and rollover mechanism. This is not provided by Livingdocs.

#### Elastic

To support search and delivery Livingdocs uses [elasticsearch](https://www.elastic.co/). We support version 1.7 and upwards. Some feature might require addition configuration.

You will also want to think about your replication strategy. 

#### Cloud storage

In order to store files such as images and CSS resources, Livingdocs supports cloud storage compatible with the Amazon S3 API.

You will need to take care about backups of the buckets yourself.

#### Pusher (optional)

[Pusher](https://pusher.com) is used to support real-time collaboration of several writers within Livingdocs. To our knowledge there is no way to install pusher locally and you need to use the service they provide. Your pusher account can be configured in the server's configuration file.

You can deactivate pusher in the editor's configuration file.

#### newrelic (optional)

In order to track your server's sanity, Livingdocs supports [newrelic](http://newrelic.com/). You can configure your newrelic account in the server's configuration file.

#### Google analytics (optional)

For the public delivery of the server (the "Public Link" on livingdocs-beta.io) you can enable [Google analytics](http://www.google.com/analytics/). You can configure your analytics account in the server's configuration file.   

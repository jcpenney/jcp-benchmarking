## Configure Buildpack

To install [Siege](http://www.joedog.org/siege-home/), configure Heroku to download the [siege-dyno buildpack](https://github.com/jcpenney/siege-dyno) with the following command:
	
	heroku config:set BUILDPACK_URL=https://github.com/jcpenney/siege-dyno
	
## Run Siege

Once Siege is installed, run load tests using the `heroku run ./siege` command, e.g.:

	heroku run ./siege http://yourdomain.com/ -c 20 -r 100 
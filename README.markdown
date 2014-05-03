## Configure Buildpacks

Configure Heroku to use the [buildpack-multi](To install [Siege](http://www.joedog.org/siege-home/) with the following command:
	
	heroku config:set BUILDPACK_URL=http://www.joedog.org/siege-home/

Then, to install [Siege](http://www.joedog.org/siege-home/), be sure that the [siege-dyno buildpack](https://github.com/jcpenney/siege-dyno) is specified in `.buildpacks`.
	
## Run Siege

Once Siege is installed, run load tests using the `heroku run ./siege` command, e.g.:

	heroku run ./siege http://yourdomain.com/ -c 20 -r 100 
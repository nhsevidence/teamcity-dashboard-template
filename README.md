# Team city dashboard based on dashing

This project contains a teamcity dashboard template based on the [Dashing](http://dashing.io/) dashboard framework with a [teamcity widget](https://gist.github.com/makepanic/a87e96dfd21583b96eb3#file-team_city-html) running in a docker container.    

# Configuration

You need to provide environment variables for the following settings:
* TC_SERVER_URL (teamcity server url i.e 'http://yourteamcityserver/httpAuth/app/rest/')
* TC_USER (teamcity username)
* TC_PASSWORD (teamcity password)


## Adding dashboards
Add dashboards by adding files to the dashing directory called 'dashboardname.erb'

## Adding teamcity projects
See the config/teamcity.yml file for adding projects.  The key value pairs under 'repositories' in the yml - the key should correspond to the 'data-id' attribute in the dashboard/yourdashboard.erb file.  Currently only top level projects with subprojects are supported by the teamcity job (we could change this).

# Running it up

Make sure to set the environment variables and configured your projects mentioned above.  To run the dashboard server up run this command in same directory as the docker-compose.yml file:

```
docker-compose up -d
```

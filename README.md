# Team city dashboard based on dashing

This project contains a docker container running the ruby dashing framework with a teamcity widget template.  

# Configuration

You need to provide environment variables for the following settings:
* TC_SERVER_URL (teamcity server url i.e 'http://yourteamcityserver/httpAuth/app/rest/')
* TC_USER (teamcity username)
* TC_PASSWORD (teamcity password)

# Adding teamcity projects
See the config/teamcity.yml file for adding projects

# Adding dashboards
Add dashboards by adding files to the dashing directory called 'dashboardname.erb'

# Running it up

Make sure to set the environment variables mentioned above.  To run the dashboard server up run this command in same directory as the docker-compose.yml file:

```
docker-compose up -d
```

#StatusDashboard-Server

Embeds [statusdashboard](https://github.com/obazoud/statusdashboard). 

## Deploy

    git clone http://github.com/chamerling/statusdashboard-server.git
    cd statusdashboard-server
    heroku login
    # ... 
    heroku create
    # Will create all the required stuff on heroku (git repository) and add a remote in your git repository. Takes 5 seconds.
    git push heroku master
    # Some hooks will detect the nodejs app, launch npm... Takes 30 seconds.
    heroku open
    
The 'heroku open' commands open the browser to the newly deployed application. That's all, your monitoring app is running and polling services...

## Notes

The application is deployed on Heroku at http://YOURAPP.herokuapp.com and periodically pings defined services. In order to keep it alive, the application also pings itself with the statusdashboard heartbeat plugin. When deploying for the first time, the HEARTBEAT_URL must be set like

    heroku config:add HEARTBEAT_URL=http://YOURAPP.herokuapp.com

## License

(The MIT License)

Copyright (c) 2013 [Christophe Hamerling] (http://chamerling.org)  

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
IN THE SOFTWARE.
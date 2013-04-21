
DEMO wunderlist.aws.af.cm

# Wunderlist 2 Api v. 1

> Node.JS Wunderlist 2 Api (v1) Wrapper

## Installation
```bash
git clone https://github.com/rushis/Wunderlist2ApiJS.git
npm install request
```
## Usage 

``` js
var wl        = require('./api')
  , username  = 'you email'
  , password  = 'you password'
  , loginData = '{"email":"'+username+'","password":"'+password+'"}'

wl.login(loginData, function(error, login){
    if(login){
      wl.setApiKey(login.token)

      // Get /me
      wl.getMe(function(error, me){
        console.log('About Me -----------------------------------------')
        console.log(me)
      });

      // Get /me/settings
      wl.getMeSettings(function(error, settings){
        console.log('Settings -----------------------------------------')
        console.log(settings)        
      });   

      // Get /me/events
      wl.getMeEvents(function(error, events){
        console.log('Events -----------------------------------------')
        console.log(events)        
      });     

      // Get /me/freinds
      wl.getMeFriends(function(error, freinds){
        console.log('Freinds -----------------------------------------')
        console.log(freinds)        
      });

      // Get /me/services
      wl.getMeServices(function(error, services){
        console.log('Services -----------------------------------------')
        console.log(services)        
      });   

      // Get /me/shares
      wl.getMeShares(function(error, shares){
        console.log('Shares -----------------------------------------')
        console.log(shares)        
      }); 

      // Get /me/reminders
      wl.getMeReminders(function(error, reminders){
        console.log('Reminders -----------------------------------------')
        console.log(reminders)        
      });          
 
       // Get /me/tasks
      wl.getMeTasks(function(error, tasks){
        console.log('Tasks me all -----------------------------------------')
        console.log(tasks)        
      });         
    } else {
      console.log(error)
    }    
});
```

## API Coverage

### Implemented

``` scala

POST    /login 
GET     /me
GET     /me/settings
GET     /me/events
GET     /me/friends
GET     /me/services
GET     /me/shares

GET     /me/tasks
POST    /me/tasks
PUT     /me/<task_id>
DELETE  /me/<task_id>

GET     /me/lists
POST    /me/lists
PUT     /me/<list_id>
DELETE  /me/<list_id>

```


## License (MIT)

Copyright (c) 2012, Ruslan Khissamov.

**

### Author: [Ruslan Khissamov][0]

[0]: http://github.com/rushis/

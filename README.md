# MockServerSample
### Moco exploration 

#### What is Moco? 

A simple build simulation server library ortools.   

https://github.com/dreamhead/moco  

### Moco Installation configuration  

#### Download jar 
#### Compile run  

- Configure Java environment variables 

- Install and configure Gradle (ref:http://www.gradle.org) 

- Then get the source code: https://github.com/dreamhead/moco 

- Enter code directory,
./gradle build 

- Write JSON  

"response": {
    "json": {
      "success": 0,
      "msg": "string",
      "data": [{
        "categoryId": 1,
        "title": "Operation notice",
        "unreadCount": 0
      }, {
        "categoryId": 2,
        "title": "My offer",
        "unreadCount": 0
      }, {
        "categoryId": 3,
        "title": "Order note",
        "unreadCount": 0
      }, {
        "categoryId": 4,
        "title": "Event notification",
        "unreadCount": 0
      }, {
        "categoryId": 5,
        "title": "Commodity notification",
        "unreadCount": 0
      }]
    }
  }
}  
- After you write the JSON, you can start it    

#### java -jar moco-runner-<version>-standalone.jar start -p 12306 -c foo.json    

Then you can access it via http://localhost:12306   
In addition to Get, request patterns such as Post, Put, and Delete are naturally supported:  
[{
  "request" :
    {
      "method" : "post",
      "forms" :
        {
          "name" : "onecoder"
        }
    },
  "response" : 
    {
      "text" : "Hi."
    }}]    
    
    The configuration of the request information for Header, Cookies, etc. is also supported.

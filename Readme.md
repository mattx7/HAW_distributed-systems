Login to HAW something
> ssh -p 443 A-kennung@141.22.34.22

from there:
> ssh -p 22 root@172.19.0.43 (ip from our docker thingy)

to ask for blackbord service with netcat
> netcat -ulp 24000

we receive {"blackboard_port":5000}

to login to 172.19.0.3 (the blackboard) port 5000

see all registerd users: curl 172.19.0.3:5000/users

Register a /users with this post ( {“name”:”<user>”, “password”:”<pass>”} )

Login via get /login and receive your authentication token

check your login via whoami
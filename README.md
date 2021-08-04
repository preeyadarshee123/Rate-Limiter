# Rate-Limiter

Idea:-

We can have a sorted set with key as user id and score as time stamp . 

When a new request comes , let the time stamp be x . then all the keys with the current user id whose time stamp is less than 60 seconds should be deleted. then we can count the number of keys in the set with the current user id. if its less than 10 , then we insert the timestamp and request of current user into the set and serve the request otherwise we prompt service denied.

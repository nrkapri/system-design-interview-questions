#Design Tiny URL 

Requirements:
1. given a large URL the service will return a shorter url
2. User should be able to retrieve actual URL when the short URL is given.

Scale:
read heavy system  100:1 read : write 

Write transactions   : everyday 1 million 
Read transaction :  everyday 100 million 

latency is important 
consistency -- eventual consistency is ok 
Availability  -- more important 

Operations :

1. short_url shortenUrl(long_url)
    short_url= hash(long_url+counter)
    

2. long_url redirect(short_url)




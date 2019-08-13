
![Version](https://img.shields.io/badge/version-0.6.2-orange.svg)  
![Maintained YES](https://img.shields.io/badge/Maintained%3F-yes-green.svg)  
![Ask Me Anything !](https://img.shields.io/badge/Ask%20me-anything-1abc9c.svg)  

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/ct/ct64r.png?raw=true) **ONLINE TOOLS ([codetabs.com](https://codetabs.com))** 

version 0.6.2

1. [Count LOC (lines of code) online from github repos or zipped uploaded folder](#count-loc-online)  
2. [CORS proxy](#cors-proxy)  
3. [Github Stars graphical history](#github-stars-graphical-history)  
4. [Alexa Ranking](#alexa)  
5. [HTTP Headers](#headers)  
6. [API weather temp](#weather)  
7. [Video To Gif](#video2gif)

<hr>

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/loc48.png?raw=true) **COUNT LOC ONLINE** 

### **[DEMO and DOCS online](https://codetabs.com/count-loc/count-loc-online.html)**

- Enter user/repo , then click add or select a zipped folder and upload it  
- File max size 200mb;
- Petitions are limited to 1 every 5 secs. You will get a 429 error if you exceed  
- You can edit the colors of the segments by clicking on any point of it.
Segment will randomly change color as it is clicked.  

![Example](https://github.com/jolav/codetabs/blob/master/www/_public/images/locExample.png?raw=true)

**API LOC**

*  Make a GET HTTP Request   
`https://api.codetabs.com/v1/loc?github=USERNAME/REPONAME`

Example :   
https://api.codetabs.com/v1/loc?github=jolav/codetabs

Response (JSON) :

```json
[
 {
  "language": "JavaScript",
  "files": 1,
  "lines": 176,
  "blanks": 14,
  "comments": 6,
  "linesOfCode": 156
 },   
 ... more languages
 {
  "language": "Total",
  "files": 8,
  "lines": 921,
  "blanks": 132,
  "comments": 46,
  "linesOfCode": 743
 }
]
```

<hr>

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/proxy48.png?raw=true) **CORS-PROXY**

### **[Read DOCS online](https://codetabs.com/cors-proxy/cors-proxy.html)**

- Free CORS proxy server to bypass same-origin policy related to performing standard AJAX requests to 3rd party services.
You can use to prevent mixed content of images and JSON data proxying the resources to serve them under https.
- API URL => append the url with the resource you want to "https://api.codetabs.com/v1/proxy/"
- Each request is limited to 5mb (2mb for old endpoint) size download to avoid abuse.
- Only suppports GET request.
- Limit : 5 request per second. Once reached subsequent requests will result in error 429 (too many requests) until your quota is cleared. 

<hr>

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/stars48.png?raw=true) **GITHUB STARS GRAPHICAL HISTORY**

### **[DEMO online](https://codetabs.com/github-stars/github-star-history.html)**

- Enter user/repo , then click add.
- Petitions are limited to 1 every 5 secs. You will get a 429 error if you exceed  
- You can edit the colors of the lines by clicking on any point of it. Line will randomly change color as it is clicked.  

![Example](https://github.com/jolav/codetabs/blob/master/www/_public/images/starExample.png?raw=true)

<hr>

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/alexa48.png?raw=true) **ALEXA**

Tool for know Alexa Ranking Top 1 million about a website.  

### **[Get Alexa Ranking Online](https://codetabs.com/alexa/alexa-ranking.html)**

- Petitions are limited to 5 per second. You will get a 429 error if you exceed  

<hr>

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/headers48.png?raw=true) **HEADERS**

Tool to get list of response headers including redirect chain of a HTTP connection

### **[DEMO and DOCS online](https://codetabs.com/http-headers/headers.html)**

- Petitions are limited to 5 per second. You will get a 429 error if you exceed

<hr>

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/weather48.png?raw=true) **WEATHER** 

### **[Read DOCS online](https://codetabs.com/weather/weather.html)**

- Petitions are limited to 5 per sec. You will get a 429 error if you exceed 
- CORS is enabled allowing Javascript make requests across domain boundaries
- Supported formats, json and xml  

<hr>

# ![logo](https://github.com/jolav/codetabs/blob/master/www/_public/icons/gif48.png?raw=true) **VIDEO2GIF**

### **[Video2Gif Converter online](https://codetabs.com/video2gif/video-to-gif.html)**

- Tool for converting videos to animated gifs
- File max size 100mb
- Limit : 1 request every 30 seconds. Once reached subsequent requests will result in error 429 (too many requests) until your quota is cleared.

**Parameters** 

Frames : Set frame rate (frames per second). Max value 10, default 5.

Start : Seek to given time position in seconds. "hh:mm:ss" syntax is also supported. Default is from start
> - 100 - begin from second 100   
> - 01:40 - begin from minute 1 and second 40  

Duration : Restrict the captured video sequence to the duration specified in seconds. "hh:mm:ss" syntax is also supported. Default is all duration
> - 200 - take 200 seconds from start  
> - 03:20 - take 3 minutes and 20 seconds from start  

Scale : Set width:height , if one parameter is -1 it will automatically determine the other while preserving the aspect ratio. Default is 320:160. Max 480.
> - 480:480 set width = 480 and height = 480  
> - 380:-1 set width = 380 and height automatically preserving the aspect ratio  
> - -1:320 set height = 320 and width automatically preserving the aspect ratio  

<hr>

## **Acknowledgment**

* This site includes Curtis Gagliardi <a href="https://github.com/cgag/loc">cgag/loc</a> for counting lines of code.

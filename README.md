# Video.js - HTML5 Video Player with advertisement random positions and Streaming MPEG-DASH

  Streaming MPEG-DASH is now available.

**Videojs** is a plugin

# Guides
##Getting Started##
####Add an HTML5 video tag to your page.####

```
<video id="example_video_1" class="video-js vjs-default-skin vjs-big-play-centered" controls preload="auto" width="640" height="264" data-setup="{}">
  <source src="http://dash.edgesuite.net/akamai/test/caption_test/ElephantsDream/elephants_dream_480p_heaac5_1.mpd" type='application/dash+xml'>
    <p class="vjs-no-js">To view this video please enable JavaScript, and consider upgrading to a web browser that <a href="http://videojs.com/html5-video-support/" target="_blank">supports HTML5 video</a></p>
</video>
```

After copy and paste this javascript code under HTML5 video tag.

```
<script>
    videojs('example_video_1', {
                    plugins: {
                        'myPlugin':{
                            advertisement: {
                                optional: "bottom",  // Set option "bottom" or "random"
                                setTimeStart: 2,  // Set number of seconds to show ads
                                setAdvertisementTime: 15, // Set total duration shows ads 
                                contentAds: "Hey! I'm here", // Set null to disappear ads
                            },
                            wideScreen: {
                                Width: 640, // Set width size for screen
                                Height: 480 // Set height size for screen
                            }
                        }
                    },
    
    }, function() { });

</script>
```

##Version##
0.1.0


## Browser Support##
HTML5 video support for MPEG-DASH as of today:

Chrome 23+ with H264/AAC MP4 format

IE 11 on Windows 8+ with H264/AAC MP4 format

Opera 20+ with VP8/VP9 video and Vorbis/Opus audio in WebM format

Firefox 33 does not support [MediaSource](https://developer.mozilla.org/en-US/docs/Web/API/MediaSource) by default as of today. You can activate it after switching the about:config preference media.mediasource.enabled to true.
Safari 8+ on Mac OS X Yosemite (10.10)

iOS 8 Safari does not provide support

Chrome 34+ on Android 4.2+

Live can be erratic but begins to be stable.

Note: MPEG-DASH is not as such a streaming protocol, it is a container format like MPEG-4 (ie the MPEG in MPEG-DASH) the delivery protocol being HTTP

##License##
Video.js is licensed under the Apache License, Version 2.0. [View the license file](http://www.apache.org/licenses/LICENSE-2.0)

Copyright 2014 Brightcove, Inc.

##Special Thank You##
Thanks to Steve Heffernan for the amazing Video.js and to John Hurliman for the original version of the YouTube tech

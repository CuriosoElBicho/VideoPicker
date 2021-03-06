Umbraco.VideoPicker
=======
Package for umbraco **4.x/6.x** that stores multiples videos URL's with extra properties (also can be used to save lists of asstes, like media, links, pdf's, etc).

**properties:**

*   Id 
*   Title
*   Hash    *(Url or identifier that point to the asset)*
*   Description
*   Media Id *(Provided by the native media picker of umbraco)*

**The list of videos or assets are stored in JSON fromat with the following structure:**

```
[
    {
        "id": 0,
        "title": "title of video",
        "hash": "http://vimeo.com/user12113503/httpvimeocomthejackal",
        "desc": "Description for video 0",
        "mediaId": "1052"
    },
    {
        "id": 1,
        "title": "title of video 2",
        "hash": "http://youtu.be/_646NA4sxJ8",
        "desc": "",
        "mediaId": "1049"
    },
    {
        "id": 2,
        "title": "title of video 3",
        "hash": "http://video.mp4",
        "desc": "lorem ipsum",
        "mediaId": "1051"
    }
]
```
Umbraco Package Installer
=======

[Umbraco.VideoPicker](https://github.com/eerrecart/VideoPicker/blob/master/Umbraco.Packages/Umbraco.VideoPicker.v6.x_1.0.zip?raw=true) (Working on umbraco v4.x and v6.x)

Install and Setup
=======

1. Install the package.
2. Create a new Data Type (Developer -> Data Types), select "umbraco usercontrol wrapper" as property editor. Save the data type.
3. On the settings section of the data type created in the previus step select as user control: `~/usercontrols/Umbraco.VideoPicker/VideoPickerDatatype.ascx`. Save the data type.
4. On the doc type of your choice add a new property using the Type created on step 3. (If you wish to install the example package, the macro uses a property called _video_.)
5. Now the documents based on the doc type choosen on step 4, will have the video picker component.

Umbraco Package Example Installer
=======

[Umbraco.VideoPicker.Example](https://github.com/eerrecart/VideoPicker/blob/master/Umbraco.Packages/Umbraco.VideoPicker.Example.v6.x_1.0.zip?raw=true) (Working on umbraco v6.x)

This macro (can be easly refactored to work in umbraco **v4.x**) shows how to query the data stored form the VideoPicker and get it on the front end page. Then using the embed.ly (uses [oEmbed](http://oembed.com/) standard) provider get the videos from: *youtube*, *vimeo*, or any other supported by embed.ly.
Also you can build your own provider.

License
-------

The MIT License (MIT)

Copyright (c) 2013 Elias Errecart

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
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

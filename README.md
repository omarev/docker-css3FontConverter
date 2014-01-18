docker-css3FontConverter
========================

css3FontConverter (https://github.com/zoltan-dulac/css3FontConverter) enables you to convert TTF/OTF fonts to EOT, SVG, WOFF and in the same time generates CSS stylesheet with CSS3 @font-face ready for use.

To start using css3FontConverter you can either download the image or build it by yourself. Both options have their advantages.

#### How to Download ####
$ `sudo docker pull omarev/css3-font-converter`

#### How to Build ####

Fetch the code

$ `git clone https://github.com/omarev/docker-css3FontConverter.git`

Change directory

$ `cd docker-css3FontConverter`

Build

$ `sudo docker build -t omarev/css3-font-converter .`

#### How to run the container ####

$ `sudo docker run -v /path/to/font/files:/fonts -i -t omarev/css3-font-converter /bin/bash`

This command will attach this host path `/path/to/font/files` to `/fonts` directory inside the container

#### How to convert fonts ####

##### Inside the container: #####

Go to the directory with the fonts

$ `cd /fonts`

Do the conversion

$ `/css3FontConverter/convertFonts.sh *.ttf`

That was it, now exit the container by typing `exit` and then check your directory with the fonts.

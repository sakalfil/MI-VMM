# MI-VMM
Picture similarity retrieval with SURF

=======
## This is semestral project for subject MI-VMM@FIT-CTU
It contains 2 main parts:
* Interest points finder (folder ipmatching/public/ipfinder)
 * jopensurf library (https://code.google.com/archive/p/jopensurf)
* IP matching & Web app (folder ipmatching)
 * Ruby on Rails app
 * This app will call ipfinder on every uploaded picture in order to get Interest Points.
 
## Usage
1. Interest point finder
```sh
$ java -jar "public/ipfinder/dist/semestralka.jar" file1 file2 ...
```

Example output:
```sh
Surf Interest Points Finder:
446.79404 37.28289
446.19263 45.850067
451.79227 48.068607
462.39285 52.582752
354.75287 53.189285
448.75555 59.47033
...
```

2. Web app
 1. Rails installation (ruby, rubygems, ...)
 2. Run rails server
```sh
$ cd MI-VMM
$ bundle install
$ nano config/database.yml # setup mysql database
$ rake db:create db:migrate
$ rails server
```
And show it in your browser (default address is localhost:3000).

# Overview
This is a demo made up of three seperate ones and is intended to be used in datastax developer days.

It includes:
* Search demo that showcases geospacial searching.
* DSE Anylytics notebook that uses spark SQL.
* Graph Notebook that showcases DSE Graph basic usage.

# Instructions/Project setup
* If using AssetHub use at least a m3.2xLarge cluster.
* If using the dsa scripts use command `python dsa-ec2.py start YOURCLUSTERNAME 1 -c developer-day -t m5.2xlarge` replaceing the cluster name with the one you want. 

To set up the demo on a dsa instance:
```
cd /tmp
git clone https://github.com/mando222/SDDemos.git
cd SDDemo
sudo ./startup all
# Total setup should be about 2 hours to complete
# Start geo app
java -jar target/geofinder-api.jar -h node1
```
The AssetHub version should work without user setup commands.

## Search Demo
This is a simple web app to demonstrate some of the geospatial capabilities in DSE.  It is not meant to be a demonstration of how to build a REST API. I used the [spark java framework](http://sparkjava.com/) (not to be confused with Apache Spark) for its lean and simple approach.

The web app is exposed on port 9000

If you are running this from assethub, you will need to point your web browser at:

http://node0_ip:9000

If you are running this from the dsa scripts, you will need to point your web browser at:
http://node1_ip:9000

## DSE Graph and Analytics Demos
Start exploring using DataStax Studio 6!

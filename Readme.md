## TopoJSON Command line Cartography 

This docker installs Topojson in a docker container so you can use docker to run the topojson command line tools!

How to build:

	docker build -t niene/topojson .

To run the topojson help :

	docker run --rm niene/topojson topomerge -h
	docker run --rm niene/topojson toposimplify -h
	docker run --rm niene/topojson topo2geo -h
	docker run --rm niene/topojson geo2topo -h


To run topojson with options:

	docker run --rm -v $(pwd)/input_data:/data_in niene/topojson topomerge [options] <target=source> [file]
	docker run --rm -v $(pwd)/input_data:/data_in niene/topojson toposimplify [options] <file>
	docker run --rm -v $(pwd)/input_data:/data_in niene/topojson topo2geo [options] <name=file>…
	docker run --rm -v $(pwd)/input_data:/data_in niene/topojson geo2topo [options] <[name=]file>…

See 

* https://github.com/topojson/topojson/blob/master/README.md#api-reference 
* https://medium.com/@mbostock/command-line-cartography-part-3-1158e4c55a1e

docker-varscoper
=======================

Run the varscoper CFML code analysis tool from a Docker container.

## Installation
1. Pull image

	```
	sudo docker pull boomfish/varscoper
	```

## Usage
1. Create and run a varscoper container that publishes container port 8888 to your host and maps the HTML source you want to analyse to a subfolder of the webapp root in the container:

	```
	sudo docker run -v /path/to/my/src:/opt/railo/tomcat/webapps/ROOT/src -p 48009:8888 --rm boomfish/varscoper
	```
2.  Once you see a "Server startup" message in the Docker terminal, open a browser to the published port on the host http://localhost:48009 and enter the mapped subfolder name as the location to scan.

3. When you are finished scanning, go back to the Docker terminal and press `Ctrl-C` to stop and delete the container.

## License

This code is available under the [MIT License](LICENSE.txt).

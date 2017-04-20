## ccldap

A basic configuration of OpenLDAP server with Compute Canada schema and
mock account data.

Installation:

1) Ensure Docker is installed: https://www.docker.com/get-docker

2) Ensure that you are on a machine that can run a Debian Jessie based docker image

3) Go to the image directory and build the docker container:

	docker build -t ccldap .

4) Run the container:

	docker run --env LDAP_ORGANISATION="Compute Canada" --env LDAP_DOMAIN="computecanada.ca" --detach ccldap
	Exposed to a port:
	docker run -p 3389:389 --env LDAP_ORGANISATION="Compute Canada" --env LDAP_DOMAIN="computecanada.ca" --detach ccldap


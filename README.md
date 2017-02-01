# Java Hello World

This is a demo Java Lambda function setup in the Serverless framework, using Maven.

A demo of this service can be found here, https://kkpai1pyz5.execute-api.eu-west-1.amazonaws.com/v0/hello

#### Getting Started

Ensure you have both the [Docker Toolbox](https://www.docker.com/products/docker-toolbox) and [Serverless](https://www.npmjs.com/package/serverless) installed and configured.

To build the project run:

`$ docker-compose build && docker-compose run hello-world`

To deploy the project:

`$ sls deploy --stage <beta|v0|v1|prod|etc> --region <aws region>`

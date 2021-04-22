[![cdk](https://img.shields.io/badge/built%20with-cdk-%23ec7211)](https://aws.amazon.com/cdk/)
[![SonarCloud](https://sonarcloud.io/images/project_badges/sonarcloud-orange.svg)](https://sonarcloud.io/dashboard?id=pawarrchetan_cdk-construct)
# A serverless app using AWS CDK and Projen

This is a serverless project using TypeScript with AWS CDK.
This is a simple project setup using Projen

## Requirements

* Node version 14 or later
* npm version 7 or later
* awscli v2
* [AWS CDK Toolkit](https://aws.amazon.com/cdk/)
* [Projen](https://github.com/projen/projen)

## Components

* AWS API Gateway
* AWS Lambda Function

## Getting Started

To start the Development, 
* Clone the project to your local machine 
``` 
git clone <repository-name>
```

* Run `yarn install` to setup the package dependencies in the root project.
```
yarn install
```

* Use the projen commands to refelct any changes to the code.
```
npx projen
```

## Useful Commands
The `cdk.json` file tells the CDK Toolkit how to execute your app.

 * `npx projen build`   compile typescript to js
 * `npx projen watch`   watch for changes and compile
 * `yarn test`    perform the jest unit tests

## Building

To build the project, run `yarn build` in the root project. This command will run npm run build on all packages.

## Testing

Various scripts are predefined in the `package.json` generated from projen.

Run the test with `yarn test`.
`yarn build `also runs test, so omit the example output here.

## Sonar Scanning
The project has been used SAST from Sonarcloud to generate a report about the critical components in the project.
The link for the report can be found [Sonarcloud Report](https://sonarcloud.io/dashboard?id=pawarrchetan_cdk-construct).

## Deploy Locally

* Once the build is successful, try deploying locally.
```
$ cdk deploy --app='./lib/integ.default.js'
```

* You can check the response of the Lambda function from the output API URL.
```
$ curl https://4p9zxdfgy8.execute-api.ap-northeast-1.amazonaws.com/
"Hello from Lambda!"
```

* To delete  the deployment.
```
$ cdk destroy --app='./lib/integ.default.js'
```

## License

MIT License
CI/CD Pipelines


CircleCI has been configured so that it executes the pipeline with every push to the configured GitHub repository. The workflow consists of 2 jobs, one for building and deploying the Backend and another for building and deploying Frontend. The package.json in the Udagram directory contains scripts used by CircleCI. These scripts call specific scripts in package.json files. This makes the CircleCI configuration script easier to read.

Backend
As part of the initial setup the AWS CLI and Elastic Beanstalk CLI are installed. The necessary environment variables configured in the project are set within CircleCI for deployment and Elastic Beanstalk for running the application. After the dependencies are installed the build process starts. It copies over only the necessary node modules and Elastic Beanstalk configurations. After build, the Elastic Beanstalk CLI is used to deploy the files to AWS.

Frontend
For this job, the AWS CLI is installed. Before the dependencies are installed, Angular CLI is installed in a docker environment. The Angular CLI is used to lint and build the codebase. The production build will make sure that the deployed code is small and minified as well as optimized. The AWS CLI is used to sync the existing files and the S3 bucket.
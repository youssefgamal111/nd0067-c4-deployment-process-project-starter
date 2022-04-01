Infrastructure
AWS setup
The production setup of this project is based on AWS. A simple diagram of the infrastructure is shown below.



Database
The database is hosted on AWS RDS .database-1.c0pobhoqf6mu.us-east-1.rds.amazonaws.com

Backend
The backend is hosted on AWS Elastic Beanstalk. Udagram-env.eba-xh33ykty.us-east-1.elasticbeanstalk.com  is the backend endpoint.

The platfrom is based on Node.js 14 running on 64bit Amazon Linux 2/5.4.10.

Database connection and Secrets are configured using Environment Variables.

Frontend
The frontend is hosted on AWS S3 that is publicly accessible. http://udagram-frontendpro2.s3-website-us-east-1.amazonaws.com is the frontend endpoint.


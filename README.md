# AWS-Wordpress-App

In this hands-on project we are going to improve and scale the architecture of a wordpress web application. The architecture will start with a manually built single instance, running the application and database over the stages of the project you will evolve this until its a scalable and resilient architecture.

The demo consists of 5 stages, each implementing additional components of the architecture

* [Stage 1](Lab_Instructions/Step1.md) - Create a Stack and Configure SSM Parameters
* [Stage 2](Lab_Instructions/Step2.md) - Automate the build using a Launch Template
* [Stage 3](Lab_Instructions/Step3.md) - Split out the DB into RDS and Update the LT
* [Stage 4](Lab_Instructions/Step4.md) - Split out the WP filesystem into EFS and Update the LT
* [Stage 5](Lab_Instructions/Step5.md) - Enable elasticity via a ASG & ALB and fix wordpress (hardcoded WPHOME)

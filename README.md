# AWS Continuous Integration

# Set Up GitHub Repository
The first step for Continuous Integration is to set up a GitHub repository to store the Python application's source code. 

# Create an AWS CodePipeline
An AWS CodePipeline is created to automate the continuous integration process for the Python application. AWS CodePipeline will orchestrate the flow of changes from the GitHub repository to the deployment of the application

1. Go to the AWS Management Console and navigate to the AWS CodePipeline service.
2. Click on the "Create pipeline" button.
3. Provide a name for your pipeline and click on the "Next" button.
4. For the source stage, select "GitHub" as the source provider.
5. Connect your GitHub account to AWS CodePipeline and select your repository.
6. Choose the branch you want to use for your pipeline.
7. In the build stage, select "AWS CodeBuild" as the build provider.
8. Create a new CodeBuild project by clicking on the "Create project" button.
9. Configure the CodeBuild project with the necessary settings for your Python application, such as the build environment,    build commands, and artifacts.
10. Save the CodeBuild project and go back to CodePipeline.
11. Continue configuring the pipeline stages, such as deploying your application using AWS Elastic Beanstalk or any other suitable deployment option.
12. Review the pipeline configuration and click on the "Create pipeline" button to create your AWS CodePipeline.

# Configure AWS CodeBuild
In this step, AWS CodeBuild is configured to build the Python application based on the specifications we define. CodeBuild will take care of building and packaging the application for deployment.
Codebuild is configured from the AWS Management console
1. CodeBuild Project is named as: sample-python-flask-app
2. Source provider: AWS CodePipeline
3. Select the pipeline created in the previous step
4. Configure the build environment, such as the operating system, runtime, and compute resources required for your Python application.
5. Specify the build commands, such as installing dependencies and running tests. Customize this based on the application's requirements.
6. Set up the artifacts configuration to generate the build output required for deployment.
7. Review the build project settings and click on the "Create build project" button to create your AWS CodeBuild project.

# Trigger the CI Process
Here CI process is triggered by making a change to our GitHub repository
1. In the GitHub repository and a change is made to the Python application's source code. It could be a bug fix, a new feature, or any other change you want to introduce.
2. Commit and push the changes to the branch configured in your AWS CodePipeline.
3. Head over to the AWS CodePipeline console and navigate to your pipeline.
4. The pipeline automatically kick off as soon as it detects the changes in your repository.
AWS CodePipeline takes care of the rest. It will fetch the latest code, trigger the build process with AWS CodeBuild, and deploy the application if configured the deployment stage.

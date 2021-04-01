Prerequisites:
  * Require a project with written dockerfile in it.

Steps to integrate jenkins with docker
* Download docker for windows above version 10 and incase of window 7 & below versions use docker toolbox
* Create account in docker hub
* Go to Dashboard-> manage jenkins -> manage plugins -> install various plugins for docker :
  1. CloudBees Docker Build and Publish plugin
  2. Docker plugin
  3. docker-build-step
  4. Docker Pipeline
  
  
* Now go to pom.xml of project containing dockerfile and add finalname tag and write jar name inside it.
* My custom jar name is : docker-jenkins-integration-sample

* Open created job for project and then click on Configure
* Go to build tab and select "Docker Build and Publish" from dropdown in build section
  * Add repository name as :  dockerId or username/jarname
      * Example:
          * my docker hub account username = shilparaghav
          * my jar name = docker-jenkins-integration-sample
   * So repository name will be: shilparaghav/docker-jenkins-integration-sample
   
   * Add Registry Credentials also in build section if not exist in dropdown (add username and password of dockerhub account)
   * Select added registry credentials of your own account
   
   * At last apply and then save configuration
   


              




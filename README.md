15 minute getting started:
http://pivotal.io/platform/pcf-tutorials/getting-started-with-pivotal-cloud-foundry/introduction

https://login.run.pivotal.io/login

accessing apps with SSH:
http://docs.cloudfoundry.org/devguide/deploy-apps/ssh-apps.html

#get help from cloud foundry
cf help

git clone https://github.com/cloudfoundry-samples/spring-music

cd spring-music

./gradlew assemble

#sign in
cf login -a api.run.pivotal.io

#push the app to PWS
cf push

#view the logs
cf logs spring-music --recent
cf logs spring-music

#list the available ElephantSQL plans
cf marketplace -s elephantsql

#create a service instance with the free plan
cf create-service elephantsql turtle my-spring-db

#bind newly created service to the app
cf bing-service spring-music my-spring-db

#restart the app
cf restart spring-music

#verify the service is bound to the app
cf services

#scale the app
cf scale spring-music -i 2

#check the status
cf app spring-music

#increase memory
cf scale spring-music -m 1G

#scale disk limit
cf scale spring-music -k 512M

#How PCF works:
https://docs.pivotal.io/pivotalcf/concepts

#PCF documentation
https://docs.pivotal.io/pivotalcf/installing/pcf-docs.html

#Installing PCF (Iaas-specific guides for installing PCF)
https://docs.pivotal.io/pivotalcf/installing/

#Learn more about the Spring framework
https://spring.io/guides

#Ruby example:
https://github.com/cloudfoundry-samples/pong_matcher_rails

#JS example:
https://github.com/cloudfoundry-samples/pong_matcher_sails

#python exmaple:
https://github.com/cloudfoundry-samples/pong_matcher_django

#Go example
https://github.com/cloudfoundry-samples/pong_matcher_go


##Dashboard:
https://console.run.pivotal.io/organizations/88dbdd38-293c-4ba5-9ced-c97ca424fd6b#spaces

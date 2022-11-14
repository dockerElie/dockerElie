#BUILDING A DOCKER FILE FOR POZOS
#BASE LAYER
FROM python:2.7-stretch AS base
#PERSON TO REACH IF ANY ISSUE WHILE USING THIS DOCKER FILE
MAINTAINER NONO NOUAGONG ELIE-MICHEL (eliewear1@gmail.com)
#ADD SOURCE CODE INTO OUR WORKING DIRECTORY
ADD student_age.py /
#INSTALL ANY REQUIRED DEPENDENCIES
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0
#PERSISTENT DATA
VOLUME [ "/data" ]
#EXPOSE THE API AT PORT 5000
EXPOSE 5000
#RUN APPLICATION
CMD [ "python", "./student_age.py" ]

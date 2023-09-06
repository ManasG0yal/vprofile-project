# here we use the multistage docker to create the war file in one image and export it into the other image

# using openjdk image 
FROM openjdk:11 AS BUILD_IMAGE 
RUN apt update && apt install maven -y
# cloning the code and building the pom.xml file 
RUN git clone https://github.com/ManasG0yal/vprofile-project.git
RUN cd vprofile-project/ && mvn install 

# this is the second container in it we create the tomcat image 

#using tomcat basse image 
FROM tomcat:9-jre11

LABEL "project"="containerization-vprofile"
LABEL "Author"="ManasG0yal"

# removing the base app from the tomcat 
RUN rm -rf /usr/local/tomcat/webapp/*

# copying from the first image directory, into the second image directory
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapp/ROOT.war

# exposing the port 8080 
EXPOSE 8080

# this is the base command use to run the tomcat server
CMD ["catalina.sh","run"]
pipeline {
             agent none
          
             stages {
                       stage ('war-deploy'){
                       agent {
                              label {
                                      label 'built-in'
                                       customWorkspace '/root/assignment'       
                                     }
                             }
                       tools {
                                 maven 'maven3.8.7'
                                 jdk 'java1.8.0'
                             }
                       environment{
                                       PATH = "/root/maven/apache-maven-3.8.7/bin:$PATH"
                                   }   
                                              steps{
                                                            git 'https://github.com/dishu14/game-of-life.git'    
                                                            sh 'cp /root/assignment/gameoflife-web/target/gameoflife.war /mnt/server/apache-tomcat-9.0.71/webapps/'
                                                    }           
                                                }
                           }
          }               

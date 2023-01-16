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
                      
                       environment{
                                       PATH ="/root/apache-maven-3.8.7/bin:$PATH"
                                   }   
                                              steps{
                                                            git 'https://github.com/dishu14/game-of-life.git'    
                                                            sh 'cp /root/assignment/gameoflife-web/target/gameoflife.war /mnt/server/apache-tomcat-9.0.71/webapps/'
                                                    }           
                                                }
                           }
          }               

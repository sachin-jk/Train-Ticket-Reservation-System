pipeline {
//agent any
agent {label 'slave'}

stages {
  stage('git checkout') {
    steps {
      git 'https://github.com/sachin-jk/Train-Ticket-Reservation-System.git'
    }
  }

  stage('maven build') {
    steps {
      sh 'mvn clean install'
    }
  }

  stage('push war file to webapps') {
    steps {
      sh 'sudo cp target/*.war /opt/tomcat/apache-tomcat-9.0.68/webapps/'
    }
  }

}

}

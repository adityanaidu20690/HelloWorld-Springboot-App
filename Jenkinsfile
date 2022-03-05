pipeline {
    agent any 
    stages {
        stage('Git clone') { 
            steps {
                git 'https://github.com/adityanaidu20690/HelloWorld-Springboot-App.git'
            }
        }
        stage('maven clean') { 
            steps {
                sh 'mvn clean'
            }
        }
        stage('maven package') { 
            steps {
                sh 'mvn package'
            }
        }
        stage('maven test') { 
            steps {
                sh 'mvn test'
            }
        }
        stage('Archive') { 
           steps {
              archiveArtifacts artifacts: 'target/*.jar, target/*.war', followSymlinks: false
            }
        }
   
        stage('Notify') { 
            steps {
                sh 'echo "final step"'
            }
        }
    }
}

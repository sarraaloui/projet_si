pipeline{
    agent any
    stages{
        stage('git repo & clean'){
            steps{
              //  bat "rmdir /s /q Jenkins-pipeline"
                bat "git clone https://github.com/sarraaloui/projet_si.git"
              //  bat "mvn clean -f Jenkins-pipeline"
            }
        }
        stage('install'){
            steps{
                bat "mvn install -f Jenkins-pipeline"
            }
        }

        stage('test'){
            steps{
                bat "mvn test -f Jenkins-pipeline"
            }

        }
        stage('package'){
            steps{
                bat "mvn package -f Jenkins-pipeline"
            }
        }
    }
}

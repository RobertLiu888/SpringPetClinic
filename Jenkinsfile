ipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/AnjuMeleth/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn complie'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        step('Deploy'){
            steps{
                sh 'java-jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}

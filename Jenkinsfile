pipeline {
    agent any
    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }

        stage('Send Email') { 
            steps { 
                script { 
                    def email = "vishal7738639800@gmail.com" 
                    def subject = "Build Notification" 
                    def body = "The build has completed successfully." 
                    def mailtoLink = "mailto:${email}?subject=${subject}&body=${body}" echo "Mailto link: ${mailtoLink}" 
                } 
            }
        }
    }
}

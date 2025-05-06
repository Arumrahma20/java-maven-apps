pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                script {
                    echo "Melakukan pengujian aplikasi..."
                    echo "Menjalankan pipeline untuk branch ${BRANCH_NAME}"
                }
            }
        }

        stage('Build') {
            when {
                expression { BRANCH_NAME == 'main' }
            }
            steps {
                script {
                    echo "Membangun aplikasi..."
                }
            }
        }

        stage('Deploy') {
            when {
                expression { BRANCH_NAME == 'main' }
            }
            steps {
                script {
                    echo "Melakukan deployment aplikasi..."
                }
            }
        }
    }
}

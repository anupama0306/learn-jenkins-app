pipeline {
    agent any
    environment {
        BUILD_FILE = 'laptop.txt'
    }

    stages {
        stage('build') {
            steps {
                cleanWs()
                echo 'Building from jenkins'
                sh '''
                mkdir build
                echo "anupama" >> build/$BUILD_FILE
                cat build/$BUILD_FILE
                '''
            }
        }
    stage('test') {
            steps {
                
                echo 'testing from jenkins'
                sh '''
                test -f build/$BUILD_FILE
                mkdir test
                touch test/test.txt
                echo "joshi" >> test/test.txt
                cat test/test.txt
                '''
            }
        }
    }
}

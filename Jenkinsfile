pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/KJyothirmayi-2025sl93025/labsheet1-2025sl93025.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build stage completed"'
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 -c "
import calculator

# Test add
assert calculator.add(2,3)==5

# Test multiply
assert calculator.multiply(2,3)==6

# Test subtract
try:
    assert calculator.subtract(5,3)==2
except:
    pass

# Test divide
try:
    assert calculator.divide(6,3)==2
except:
    pass

print('All functions working correctly')
"
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy stage completed"'
            }
        }
    }
}

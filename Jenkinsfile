pipeline {
    agent {
        label {
            label 'built-in'
        }
    }
    stages {
        stage ('index deploy'){
            steps {
                sh "yum install httpd -y"
                sh "service httpd start"
                sh "cp -r index.html /var/www/html"
                sh "chmod -R 777 /var/www/html/index.html"
                sh "service httpd restart"
            }
        }
    }
}
pipeline {
    agent {
        label {
            label 'built-in'
        }
    }
    stages {
        stage ('master'){
            steps {
                sh "yum install httpd -y"
                sh "service httpd start"
                sh "cp -r index.html /var/www/html"
                sh "chmod -R 777 /var/www/html/index.html"
                sh "service httpd restart"
            }
        }
        stage ('node-1'){
            agent {
                label {
                    label 'dev-172.31.4.204'
                }
            }
            steps {
                sh "yum install httpd -y"
                sh "service httpd start"
                sh "cp -r index.html /var/www/html"
                sh "chmod -R 777 /var/www/html/index.html"
                sh "service httpd restart"
            }
        }
        stage ('node-2'){
            agent {
                label {
                    label 'qa-172.31.4.221'
                }
            }
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
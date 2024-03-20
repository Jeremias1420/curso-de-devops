pipeline {
        agent any
        stages{
            stage('Buid da imagem docker'){
                steps{
                    sh 'docker buid -t /root/node-app'
                }
            }
            stage('Subir docker compose - redis e app ') {
                steps {
                    sh 'docker compose up --buid -d'
                }
            }
            stage('sleep para subida de containers'){
                steps{
                    sh 'sleep 10'
                }
            }
            stage('Teste da aplicação '){
                sleep{
                    sh 'teste-app.sh'
                }
            }
        }
    }
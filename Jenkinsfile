pipeline {
    agent any

    stages {

        stage ('Download') {
            steps {
                rtDownload (
                    serverId: "telus",
                    spec: """{
                            "files": [
                                    {
                                        "pattern": "artifactory/pss-local/PS%20Suite/build-info/master/build-26/*"
                                    }
                                ]
                            }"""
                )
                withCredentials([usernameColonPassword(credentialsId: 'artifactory_creds', variable: 'CREDS')]) {
                    sh "curl -u$CREDS -O https://srv.dev.telushealth.com/artifactory/pss/Screen%20Shot%202019-02-01%20at%209.16.28%20PM.png"
                }
                sh "pwd"
                sh "ls -al"
            }
        }
    }
}

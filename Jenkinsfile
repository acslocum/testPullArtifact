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
                                        "pattern": "pss-local/PS%20Suite/build-info/master/build-26/PSS.Build.Info.zip",
                                        "target": "test.zip"
                                    }
                                ]
                            }"""
                )
                sh "pwd"
                sh "ls -al"
                sh "unzip -l test.zip"
            }
        }
    }
}

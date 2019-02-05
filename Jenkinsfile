pipeline {
    agent any

    stages {
        stage ('Clone') {
            steps {
                git branch: 'master', url: "git@github.com:acslocum/testPullArtifact.git"
            }
        }

        stage ('Download') {
            steps {
                rtDownload (
                    serverId: "telus",
                    spec: """{
                            "files": [
                                    {
                                        "pattern": "pss/Screen%20Shot%202019-02-01%20at%209.16.28%20PM.png",
                                        "target": "test/",
                                    }
                                ]
                            }"""
                )
            }
        }
}

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
                                        "pattern": "pss/Screen%20Shot%202019-02-01%20at%209.16.28%20PM.png",
                                        "target": "test"
                                    }
                                ]
                            }"""
                )
            }
        }
    }
}

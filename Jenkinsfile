pipeline {
    agent any
    stages {
        stage('Load Branch-Specific Jenkinsfile') {
            steps {
                script {
                    def scriptPath = "Jenkinsfile-${env.BRANCH_NAME}"
                    echo "Loading ${scriptPath}"
                    def pipelineScript = load(scriptPath)
                    pipelineScript.DevPipeline()
                }
            }
        }
    }
}

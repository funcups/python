pipeline {
    agent {
        node {
            label "TestNode"
        }
    }
    options {
        timeout(time: 1, unit: "HOURS")
    }
    parameters {
        string(name: 'Smoke', defaultValue: 'smokeeeee', description: '')
        string(name: 'Prod', defaultValue: 'proddddd', description: '')
    }
    stages {
        stage("第一个"){
            when {
                environment name: 'Smoke', value: '123'
            }
            steps {
                echo "hello world"
                echo "${params.Smoke}"
            }
        }
    }
    post {
        always {
            echo "done!!!!!!!!!"
        }
    }
}

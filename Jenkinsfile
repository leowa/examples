def role
pipeline {
    agent {
      label "master"
    }
    stages {
        // stage("Select role") {
        //     input {
        //         message "Select deployment role"
        //         submitter "azhang"
        //         parameters {
        //             string(name: 'role', defaultValue: 'cn.wish.jenkins', description: 'which role to deploy?')
        //         }
        //     }
        // }
        stage('Deploy') {
            input {
                message "Select deployment environment"
                submitter "azhang"
                parameters {
                    string(name: 'environment', defaultValue: 'stage', description: 'which environment to deploy?')
                }
            }
            steps {
                echo "Apply latest state for ${role} in ${environment}"
                // # sh "sudo salt --no-color --state-output=changes -C \"G@role:${role} and G@environment:${environment}\" state.highstate"
            }
        }
    }
}


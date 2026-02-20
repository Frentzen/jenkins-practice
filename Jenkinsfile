pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }

        stage('Approval Gate') {
            steps {
                input(
                    message: 'Deploy to Production?',
                    ok: 'Yes, deploy it!',
                    submitter: 'admin,frentzen',  // ← only these users can approve
                    parameters: [
                        choice(
                            name: 'APPROVER_DECISION',
                            choices: ['Approve', 'Reject'],
                            description: 'Your decision'
                        ),
                        text(
                            name: 'APPROVER_NOTES',
                            description: 'Add any notes (optional)'
                        )
                    ]
                )
            }
        }

        stage('Deploy Production') {
            steps {
                echo 'Deploying to production...'
            }
        }
    }
}

pipeline {
  agent any
  stages {
    stage('Stage 1: Build') {
      steps {
        echo 'Task: Compile/transpile the source and produce a deployable artifact.'
        echo 'Tool: npm'
      }
    }
    stage('Stage 2: Unit and Integration Tests') {
      steps {
        echo 'Task: Execute unit tests with coverage, then run integration tests to verify component interactions.'
        echo 'Tools: Jest (unit), Postman Newman (integration)'
      }
    }
    stage('Stage 3: Code Analysis') {
      steps {
        echo 'Task: Perform static analysis for smells, complexity, duplication; generate a quality report.'
        echo 'Tool: SonarQube via SonarScanner CLI'
      }
    }
    stage('Stage 4: Security Scan') {
      steps {
        echo 'Task: Scan dependencies/source for known vulnerabilities and insecure patterns.'
        echo 'Tool: Snyk CLI'
      }
    }
    stage('Stage 5: Deploy to Staging') {
      steps {
        echo 'Task: Push the artifact to an AWS EC2 staging server and update services.'
        echo 'Tool: Ansible on AWS EC2'
      }
    }
    stage('Stage 6: Integration Tests on Staging') {
      steps {
        echo 'Task: Run the API/UI integration test suite against the staging base URL.'
        echo 'Tool: Postman Newman'
      }
    }
    stage('Stage 7: Deploy to Production') {
      steps {
        echo 'Task: Promote the tested artifact to AWS EC2 production and apply release config.'
        echo 'Tool: Ansible on AWS EC2'
      }
    }
  }
}

node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Maven';
    withSonarQubeEnv() {
      sh "${Maven}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=java1 -Dsonar.projectName='java1'"
    }
  }
}

pipeline {
  agent any

  stages {
    
    stage('Build Artifact - Maven') {
      steps {
        sh "mvn clean package -DskipTests=true"
        archive 'target/*.jar' //add a comment and as
      }
    }

    
    //stage('Unit Tests - JUnit and Jacoco') {
    //  steps {
    //    sh "mvn test"
    //  }
    //  post {
    //    always {
    //      junit 'target/surefire-reports/*.xml'
    //      jacoco execPattern: 'target/jacoco.exec'
    //    }
    //  }
    //}
//
    //stage('Mutation Tests - PIT') {
    //  steps {
    //    sh "mvn org.pitest:pitest-maven:mutationCoverage"
    //  }
    //  post {
    //    always {
    //      pitmutation mutationStatsFile: '**/target/pit-reports/**/mutations.xml'
    //    }
    //  }
    //}
//
 // //  stage('SonarQube - for SAST') {
 // //    steps {
 // //      sh "mvn sonar:sonar -Dsonar.projectKey=jenkins-pipeline -Dsonar.host.url=http://3.89.100.202:9000 -Dsonar.login=afdd917c062fd56b018d3e212403fe04c6813f61"
 // //    }
 // //  }
//
//
    // stage('Vulnerability Scan - Docker ') {
    //  steps {
    //    sh "mvn dependency-check:check"
    //  }
    //  post {
    //    always {
    //      dependencyCheckPublisher pattern: 'target/dependency-check-report.xml'
    //    }
    //  }
    //}
//
  ////  stage('Vulnerability Scan - Docker') {
  ////    steps {
  ////      parallel(
  ////        "Dependency Scan": {
  ////          sh "mvn dependency-check:check"
  ////        },
  ////        "Trivy Scan": {
  ////          sh "bash trivy-docker-image-scan.sh"
  ////        }
  ////      )
  ////    }
  ////  }
//
    //stage('Docker Build and Push') {
    //  steps {
    //    withDockerRegistry([credentialsId: "docker-hub", url: ""]) {
    //      sh 'printenv'
    //      sh 'docker build -t m46903/numeric-app:""$GIT_COMMIT"" .'
    //      sh 'docker push m46903/numeric-app:""$GIT_COMMIT""'
    //    }
    //  }
    //}
//
    //stage('Kubernetes Deployment - DEV') {
    //  steps {
    //    withKubeConfig([credentialsId: 'kubeconfig']) {
    //      sh "sed -i 's#replace#m46903/numeric-app:${GIT_COMMIT}#g' k8s_deployment_service.yaml"
    //      sh "kubectl apply -f k8s_deployment_service.yaml"
    //    }
    //  }
    //}
  }
}

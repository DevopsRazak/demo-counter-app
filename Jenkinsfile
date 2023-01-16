node('JDK8') {
     stage('sourcecode') {
        // get code from repo
        git branch: 'main', url: 'https://github.com/DevopsRazak/demo-counter-app.git'
    }
     stage('packaging the code') {
         sh 'mvn clean package'
    }  
     stage('archiving test results and artifacts') {
        // publish junit results and artifacts
       junit '/project_9/target/springboot-1.0.0.jar'
       archiveArtifacts artifacts: '/project_9/target/*.jar', followSymlinks: false
    }
}
node('JDK8'){
    stage('source code') {
        // cloning the repository from git
        git branch: 'main', url: 'https://github.com/DevopsRazak/demo-counter-app.git'
    }
    stage('building the code') {
        // building the code from maven
        sh 'mvn clean package'
    }
    stage('archiving and test results') {
        // artifacts and test results
        junit '**/target/surefire-reports/*.xml'
        archiveArtifacts artifacts: '**/*.jar', followSymlinks: false
    }
}
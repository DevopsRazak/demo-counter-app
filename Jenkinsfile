node('JDK8') {
     stage('sourcecode') {
        // get code from repo
        git branch: 'main', url: 'https://github.com/DevopsRazak/demo-counter-app.git'
    }
     stage('packaging the code') {
         sh 'mvn clean package'
    }  
     stage('archiving test results and artifacts') {
         junit '**/surefire-reports/TEST-com.example.springboot.SpringbootApplicationTests.xml'
         archiveArtifacts artifacts: '**/*.jar', followSymlinks: false
    }
}
node{
    stage("clone") {
        
        git branch: 'feature/2025.10.23', url: 'https://github.com/pavanibantu/onlinebookstore.git'
    }
     stage("Build") {
        
        bat 'mvn clean install'
    }
    stage("Test") {
        
        bat 'mvn test'
    }
     stage("Artifacts") {
        
        archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
    }
}
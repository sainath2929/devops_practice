node('UBUNTU') {
    stage('git') {
        git branch:'dev1' 'https://github.com/sainath2929/devops_practice.git'
    }
    
    stage('build') {
	sh 'mvn package'
    
    }
    
    stage('Results'){
        archive 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}
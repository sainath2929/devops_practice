node('MVN') {
    stage('git') {
        git branch:'dev' 'https://github.com/asquarezone/game-of-life.git'
    }
    
    stage('build') {
	sh 'mvn package'
    
    }
	stage('dummy'){
	sh 'pwd'
	}
    
    stage('Results'){
        archive 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}
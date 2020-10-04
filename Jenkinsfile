node {
    stage('VCS') {
        git 'https://github.com/wakaleo/game-of-life.git'
    }
    stage('Package') {
        sh 'mvn package'
    }
    stage('Archive') {
        archiveArtifacts artifacts: 'gameoflife-web/target/gameoflife.war', followSymlinks: false
    }
    stage('JUNIT') {
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}

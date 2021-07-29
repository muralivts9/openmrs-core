node('MASTER') {
    stage('SCM') {
        git 'https://github.com/muralivts9/openmrs-core.git'
    }
    stage('build') {
        sh 'mvn clean package'
    }
    stage('postbuild') {
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}
node('master') {

    stage('Pull repository from GitHub') {
        git url: 'https://github.com/browserstack/browserstack-examples-cucumber-testng.git'
    }
    stage('Checkout') {
        sh "git checkout 'iteration2_develop_reporting'"
    }


    stage('Build') {


		echo "Hello World"
		sh 'export BROWSERSTACK_USERNAME=""'
		sh 'export BROWSERSTACK_ACCESSKEY=""'
		sh 'pwd -P'
		withGradle {
            sh './gradlew build'
        }


    }
}
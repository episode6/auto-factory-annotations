#! groovy

node {
  stage('checkout') {
    checkout scm
    sh 'git submodule update --init'
  }

  def gradleRunner
  stage('pipeline') {
    gradleRunner = fileLoader.fromGit(
        'gradle/GradleRunner',
        'git@github.com:episode6/jenkins-pipelines.git',
        'v0.0.7',
        null,
        '')
  }
  
  stage('build') {
    gradleRunner.runGradle("build", "clean assemble", false)
  }

  stage('test') {
    gradleRunner.runGradle("test", "check", false)
  }

  gradleRunner.maybeDeploy()
}

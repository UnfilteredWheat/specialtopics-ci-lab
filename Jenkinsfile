
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/UnfilteredWheat/specialtopics-ci-lab'
  }

  stage('Build') {
    // you should build this repo with a maven build step here
     withMaven (maven: 'maven3') {
         sh "mvn package"
     }

    echo "hello"
  }

  try {
    stage('Test') {
        withMaven (maven: 'maven3') {
        sh "mvn package"
        }
    }
  } finally {
    junit ‘/home/CSCC/cmeyer31/IdeaProjects/specialtopics-ci-lab/**/*.xml’

  }
  // you should add a test report here
}

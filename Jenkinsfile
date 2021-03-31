
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/UnfilteredWheat/specialtopics-ci-lab'
  }

  stage('Build') {
    // you should build this repo with a maven build step here
     try {

     withMaven (maven: 'maven3') {
         sh "mvn package"
     }

     }finally {
        junit 'target/**/*.xml'
     }

    echo "hello"
  }


  // you should add a test report here
}

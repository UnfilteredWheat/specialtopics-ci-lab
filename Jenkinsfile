
node {
  stage('checkout sources') {

        git url: 'https://github.com/UnfilteredWheat/specialtopics-ci-lab'
  }

  stage('Build') {

     try {

     withMaven (maven: 'maven3') {
         sh "mvn package"
     }

     }finally {
        junit 'target/**/*.xml'
     }

    echo "hello"
  }



}

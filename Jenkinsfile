parallel build1: {node {
    stage('build') {
    deleteDir()
    checkout scm
   sh label: '', script: 'echo "Hello World" > hello.txt'
   archiveArtifacts '*.txt'
   sleep 4
    }
}
deleteDir()
}, build2: {node {
    stage('build1') {
    deleteDir()
    checkout scm
   sh label: '', script: 'echo "GoodBye World" > Goodbye.txt'
   archiveArtifacts '*.txt'
   sleep 4
    }
}
deleteDir()
}

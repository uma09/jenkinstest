parallel stage('build') {
    build1: {node {
    deleteDir()
    checkout scm
   sh label: '', script: 'echo "Hello World" > hello.txt'
   archiveArtifacts '*.txt'
   sleep 4
    }
}
deleteDir()
}, stage('build1') {
    build2: {node {
    deleteDir()
    checkout scm
   sh label: '', script: 'echo "GoodBye World" > Goodbye.txt'
   archiveArtifacts '*.txt'
   sleep 4
    }
}
deleteDir()
}

parallel build1: {node {
    deleteDir()
   sh label: '', script: 'echo "Hello World" > hello.txt'
   archiveArtifacts '*.txt'
   sleep 4
}
stage('build')
deleteDir()
}, build2: {node {
    deleteDir()
   sh label: '', script: 'echo "GoodBye World" > Goodbye.txt'
   archiveArtifacts '*.txt'
   sleep 4
}
stage('build1')
deleteDir()
}

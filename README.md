# ford
properties([pipelineTriggers([pollSCM('')])])
node{
    stage('SCM Checkout'){
        git url:'https://github.com/javahometech/my-app', branch: 'master'
    }
    stage('Welcome'){
        print "Build Got triggered, tested"
    }
}

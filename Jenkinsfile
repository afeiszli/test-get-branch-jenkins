node {
    def VERSION='null'
    def sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
    //def MY_BRANCH = sh(script: 'rev=$(git name-rev --name-only HEAD)', returnStdout: true)
    //if(env.BRANCH_NAME.contains('feature')){   
//        VERSION=getGitBranchVersion()    
//    }
    stage('Checkout'){
        //checkout scm[$class: 'LocalBranch', localBranch: "**"]
        checkout scm
        //VERSION=getGitBranchVersion()
    }
    stage('test name'){
        //sh """echo ${VERSION}"""   
        sh "echo ${MY_BRANCH}"
    }
}
def getGitBranchVersion() {
    //def content = env.BRANCH_NAME
    def content = scm.branches[1].name
    def matcher = (content =~ /feature_(.*)/)
    assert matcher.matches()    
    return matcher[0][1]
}

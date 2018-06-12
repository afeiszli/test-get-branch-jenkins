node {
    def VERSION='null'
    if(env.BRANCH_NAME.contains('feature')){   
        VERSION=getGitBranchVersion()    
    }
    stage('Checkout'){
        //checkout scm[$class: 'LocalBranch', localBranch: "**"]
        checkout scm
    }
    stage('test name'){
        sh """echo ${VERSION}"""   
    }
}
def getGitBranchVersion() {
    def content = env.BRANCH_NAME
    def matcher = (content =~ /feature_(.*)/)
    assert matcher.matches()    
    return matcher[0][1]
}

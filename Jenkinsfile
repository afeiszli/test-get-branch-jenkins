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
    def matcher = (content =~ (?<=feature).*)[0][1]
//    assert matcher.matches()    
//    return result
//    return content
    return matcher
}

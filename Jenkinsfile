node {
    def VERSION='nope'
    //if(scm.branches[0].name.contains('feature')){   
   // }
    stage('Checkout'){
        //checkout scm[$class: 'LocalBranch', localBranch: "**"]
        checkout scm
        VERSION=getGitBranchVersion()
        sh """echo env.BRANCH_NAME
    }
    stage('test name'){
        sh """echo ${VERSION}"""   
    }
}
def getGitBranchVersion() {
    def content = scm.branches[0].name
    def matcher = (content =~ /(?<=feature).*/)
    assert matcher.matches()    
//    return result
//    return content
    return matcher[0][1]
}

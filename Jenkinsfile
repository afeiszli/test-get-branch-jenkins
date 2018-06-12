node {
    if(scm.branches[0].name.contains('feature')){   
        def VERSION=getGitBranchVersion()
    }
    stage('Checkout'){
        checkout scm
    }
    stage('test name'){
        sh """echo ${BRANCH_NAME}"""   
    }
}
def getGitBranchVersion() {
    def content = scm.branches[0].name
    def result = (content =~ /(?<=feature).*/)[ 0 ]​[ 1 ]
    return result
}

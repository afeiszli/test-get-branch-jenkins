node {
    def OC_ENV=oc_env()
    def BRANCH_NAME= getGitBranchName
    stage('Checkout'){
        checkout scm
    }
    stage('test name'){
        sh """echo ${BRANCH_NAME}"""   
    }
}
def getGitBranchName() {
    return scm.branches[0].name
}

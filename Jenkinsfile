node {
    def VERSION='nope'
    //if(scm.branches[0].name.contains('feature')){   
        VERSION=getGitBranchVersion()
   // }
    stage('Checkout'){
        checkout scm
    }
    stage('test name'){
        sh """echo ${VERSION}"""   
    }
}
def getGitBranchVersion() {
    def content = scm.branches[0].name
    def result = (content =~ /(?<=feature).*/)[ 0 ][ 1 ]
    return result
}

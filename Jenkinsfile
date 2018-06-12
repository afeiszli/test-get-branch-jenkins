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
    def content = scm.branches[1].name
//    def result = (content =~ /(?<=feature_).*/)[0][1]
//    sh """echo $result"""
//    return result
    return content
}

node {
    def VERSION='nope'
    //if(scm.branches[0].name.contains('feature')){   
   // }
    stage('Checkout'){
        //checkout scm[$class: 'LocalBranch', localBranch: "**"]
        checkout scm
        VERSION=getGitBranchVersion()
    }
    stage('test name'){
        sh """echo ${VERSION}"""   
    }
}
def getGitBranchVersion() {
    def content = scm.branches[0].name
    def result = (content =~ /(?<=feature).*/)[0]
//    sh """echo $result"""
    return result
//    return content
}

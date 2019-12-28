pipeline {
   agent none
   stages{
      stage('clone') {
         steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/gh-pages']], 
            doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
            userRemoteConfigs: [[url: 'https://github.com/shashirajraja/onlinebookstore.git']]])
        }
    }
    stage('build') {
       steps {
          maven_invoker invokerBuildDir: 'target/it', reportsFilenamePattern: 'target/invoker-reports/BUILD*.xml'
          }
     }
  }
}
checkout([$class: 'GitSCM', branches: [[name: '*/gh-pages']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/shashirajraja/onlinebookstore.git']]])
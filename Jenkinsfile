pipeline{
    agent {
        label 'master'
    }
    
    environment {

    VERSION_NUMBER = VersionNumber([
        versionNumberString :'${BUILD_MONTH}.${BUILDS_TODAY}.${BUILD_NUMBER}',
        projectStartDate : '2019-02-09',
        versionPrefix : 'v'
        ])

    }

    libraries {
       lib('git_infoshared_lib@master')
    }

    stages {
       stage('Tag repo') {
           steps {
               script {
                 env.BUILD_ID = getBuildVersion()
               }
               echo 'Suyog:::::::::::::::::::'
               sh 'printenv'
               
           }
       }
    }
}


pipeline {
    agent any 
    stages {
        stage ('BUILD') { 
            steps { echo 'MAKE'}
        }
        stage ('Package : ZEY_DEVOPS_TEST' ) 
        { 
            steps { abapCi abapPackagename: 'ZEY_DEVOPS_TEST', runAtcChecks: false, runUnitTests: true, 
            sapSystemLabel: 'EYD', withCoverage: true
        }
    }
         stage ('ROLLBACK') { 
            steps { echo 'MAKE ROLLBACK'}
        }
        stage ('DEPLOY') { 
            steps { echo 'MAKE PUBLISH'}
        }
    }
}

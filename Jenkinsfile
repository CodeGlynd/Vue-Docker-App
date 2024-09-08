pipeline {
    agent any

    parameters{
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'])
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }

    stages {
      stage("build") {
        steps {
          echo 'building app...'
        }
      }

      stage("test") {
        when {
            expression {
              params.executeTests
            } 
        }
        steps {
          echo 'testing app...'
        }
      }

      stage("deploy") {
        steps {
          echo 'deploying app...'
          echo "deploying version ${params.VERSION}"



        }
      }
      
    }

}

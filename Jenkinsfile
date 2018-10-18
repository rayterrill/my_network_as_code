node {
    stage ('CheckoutRepository') {
        deleteDir()
        checkout scm
    }
    stage ('RenderConfigurations') { 
        sh 'ansible-playbook generate_configurations.yaml'
    }
    stage ('UnitTesting') { 
        // Do some kind of "linting" on our code to make sure we didn't bugger anything up too badly
    }
    stage ('DeployConfigurationstoDev') {
        // Push the configurations out to the dev environment
    }
    stage ('Functional/IntegrationTesting') {
        // Ping stuff and make sure we didn't blow up dev!
    }
    stage ('PromoteConfigurationstoProduction') {
        // Ping stuff and make sure we didn't blow up dev!
    }
    stage ('ProductionFunctional/IntegrationTesting') {
        // Ping stuff and make sure we didn't blow up prod!
    }
}

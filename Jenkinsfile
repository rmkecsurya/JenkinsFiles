pipeline{
	environment{
		PROJECT_NAME = "Surya"     //Can be used in the whole pipeline
	}
    agent any
	agent {
		label 'my-defined-agent'
	}
    stages{
        stage("Sample"){
			environment{
				CURRENT_STAGE = "CurrentStage"     //Can be used only in the stage
			}
            steps{
                echo "Hello from pipeline"
                echo "The job name is '${JOB_NAME}'"
				echo env.PROJECT_NAME
				echo env.CURRENT_STAGE
                echo currentBuild.displayName
                echo currentBuild.absoluteUrl
            }
        }
			
    }
}

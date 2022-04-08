pipeline {  
  agent any
  	triggers { 
    		GenericTrigger(
		      genericVariables: [
			[key: 'ref', value: '$.ref'],
			[key: 'changed_files', value: '$.commits[*].["modified","added"][*]'],
		      ],

	     causeString: 'Triggered on $ref', 

	     token: 'abc123',
	     tokenCredentialId: '',

	     printContributedVariables: true,
	     printPostContent: true,

	     silentResponse: false,

	     regexpFilterText: '$ref $changed_files' ,
	     regexpFilterExpression: 'refs/heads/jenkins_periodic_. .*"localDev/gateway/a".*'   
	    )
	  }
  stages {
	    stage('Some step') { 
	      	steps {
			script{
				echo "echo hii"
			}
	      }
	    }
	  }
}

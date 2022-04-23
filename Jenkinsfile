pipeline {  
  agent any
  	triggers { 
    		GenericTrigger(
		      genericVariables: [
			[key: 'ref', value: '$.ref',regexpFilter: 'refs/heads/'],
			[key: 'changed_files', value: '$.commits[*].["modified","added"][*]'],
		      ],

	     causeString: 'Triggered on $ref', 
	     token: 'abc123',
	     tokenCredentialId: '',
	     printContributedVariables: true,
	     printPostContent: true,
	     silentResponse: false,
	     regexpFilterText: '$ref' ,
	     regexpFilterExpression: 'jenkins_periodic_bcm'   
	    )
	  }
  stages {
	    stage('Some step') { 
	      	steps {
			script{
				sleep(45);
				
				
			}
	      }
	    }
	  }
}

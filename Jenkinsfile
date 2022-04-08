pipeline { 
  agent any
  	triggers { 
    		GenericTrigger(
		      genericVariables: [
			[key: 'ref', value: '$.ref', regexpFilter: 'refs/heads/'],
			[key: 'changed_files', value: '$.commits[*].["modified","added"][*]', regexpFilter: 'localDev/gateway/'],
		      ],

	     causeString: 'Triggered on $ref', 

	     token: 'abc123',
	     tokenCredentialId: '',

	     printContributedVariables: true,
	     printPostContent: true,

	     silentResponse: false,

	     regexpFilterText: '$ref $changed_files' ,
	     regexpFilterExpression: 'testing_generic New Text Document.txt'   
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

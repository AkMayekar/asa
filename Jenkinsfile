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

	     //regexpFilterText: '$ref $changed_files'
	     //regexpFilterExpression: 'refs/heads/testing_generic .*"localDev/gateway/[^"]+?".* ' 
			
	     regexpFilterText: '$changed_files'
	     regexpFilterExpression: 'README.md'
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

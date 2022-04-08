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

	     regexpFilterText: '$ref'
	     regexpFilterExpression: "refs/heads/testing_generic" //(.*"localDev/gateway/[^"]+?".*)  
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

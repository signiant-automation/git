node{

	stage 'Checkout'
	checkout scm
	
	stage 'Configuration'
	sh "make configure"
	sh "./configure"

	stage 'Build'
	sh "make"

	stage 'promotion' 
	def userInput = input( id: 'userInput', message: 'Let's promote?', parameters: [ [$class: 'TextParameterDefinition', defaultValue: 'uat', description: 'Environment', name: 'env'], [$class: 'TextParameterDefinition', defaultValue: 'uat1', description: 'Target', name: 'target'] ]) echo ("Env: "+userInput['env']) echo ("Target: "+userInput['target'])
}

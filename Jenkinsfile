#!groovy
node("master") {
    properties([
         parameters([
           string(
             defaultValue: "",
             description: "list of components",
             name: 'componentsToUpdate'
           )
         ])
       ])
    stage("branch_name") {
        checkout scm
        println "Branch name is: " + env.BRANCH_NAME
    }
    stage("check parameters") {
        println "Passed parameters: " + params.componentsToUpdate
    }
    stage("set new version to env") {
        env.UPDATED_COMPONENTS = "componentB:1.0.0"
        println "env: " + env.UPDATED_COMPONENTS
    }
}
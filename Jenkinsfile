#!groovy

// Don't test plugin compatibility - exceeds 1 hour timeout
// Allow failing tests to retry execution
// buildPlugin(failFast: false)

// Test plugin compatibility to latest Jenkins LTS
// Allow failing tests to retry execution
buildPlugin(jenkinsVersions: [null, '2.60.1'],
            findbugs: [run:true, archive:true, unstableTotalAll: '0'],
            failFast: false)

def scmVars = checkout scm
def commitHash = scmVars.GIT_COMMIT

echo commitHash

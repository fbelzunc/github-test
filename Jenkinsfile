properties([pipelineTriggers([githubPush()])])

node {
  sh 'echo Hello World!'
  node {
    checkout([$class: 'GitSCM',
        branches: [[name: '*/master']],
        doGenerateSubmoduleConfigurations: false,
        extensions: [],
        submoduleCfg: [],
        userRemoteConfigs: [[
            url: 'https://github.com/fbelzunc/github-test.git'
    ]]])
  }
}

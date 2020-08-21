# jenkins-shared-lib-demo

Using shared libraries in Jenkins

Usage:

```
stage('Git Checkout') {
    gitCheckout(
        branch: "master",
        url: "https://github.com/repo-name"
    )
}
```

Declarative Pipeline Code:

```
@Library('jenkins-shared-lib@master') _

pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
            gitCheckout(
                branch: "master",
                url: "https://github.com/repo-name"
            )
            }
    }
    }
}
```


Reference:
https://devopscube.com/create-jenkins-shared-library/
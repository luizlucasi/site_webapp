
stage 'Checkout'
node {
  git url: 'https://github.com/luizlucasi/site_webapp.git'
     withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
        sh 'mvn -B verify'
     }
     stash excludes: 'target/', includes: '**', name: 'source'
}
stage 'Build'
node {
  git url: 'https://github.com/luizlucasi/site_webapp.git'
     withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
          sh 'mvn --batch-mode -V -U -e clean package -Dsurefire.useFile=false'
     }
     stash excludes: 'target/', includes: '**', name: 'source'
}

stage 'Unit Tests'
node {
	 /* Call the Maven build with tests. */
	  mvn "install -Dmaven.test.failure.ignore=true"
	
	  /* Archive the test results */
	  step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
  }
node {
  git url: 'https://github.com/luizlucasi/site_webapp.git'
   withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
    sh 'mvn -B verify'
  }
}
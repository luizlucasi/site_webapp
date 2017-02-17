
stage 'checkout'
node {
  git url: 'https://github.com/luizlucasi/site_webapp.git'
     withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
        sh 'mvn -B verify'
     }
     stash excludes: 'target/', includes: '**', name: 'source'
}
stage 'build'
node {
  git url: 'https://github.com/luizlucasi/site_webapp.git'
     withEnv(["PATH+MAVEN=${tool 'M3'}/bin"]) {
          sh 'mvn --batch-mode -V -U -e clean package -Dsurefire.useFile=false'
     }
     stash excludes: 'target/', includes: '**', name: 'source'
}
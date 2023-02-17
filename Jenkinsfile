pipeline {
agent any
stages {
 stage ('Clone reposiory'){
 steps{
  git branch : 'main',
  url : 'https://github.com/Ekanathreddy/PES1UG20CS548_Jenkins.git'
}
 }



stage( 'Build application') {
steps {
sh 'g++ pes1ug20cs548.cpp'
}
}
stage( 'Test application') {
steps{
sh './a.out'
sh 'failure' 
}
}

}
post {
    failure {
         echo "pipeline failed "
    }
}
}

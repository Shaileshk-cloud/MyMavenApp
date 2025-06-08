pipepline{
     agent any
     tools{
     maven 'Maven'
     }
     stages{
        stage('Checkouts'){
            steps{
                 git branch:'master' ,url:'https://github.com/Shaileshk-cloud/MyMavenApp'
                 }
            }
        stage('Build'){
           steps{
                sh 'mvn clean package'
             }
        }
        stage('Test'){
          steps{
             sh 'mvn test'
            }
        }
        stage('Run Application')
        {
             steps{
                  sh'  java -jar /target/'
              }
         }
         }
         post{
              success{
                  echo 'success'
                }
              failure{
                 echo'failure'
              }
        }



}

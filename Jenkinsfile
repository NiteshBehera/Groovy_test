pipeline{
    agent any
    stages{
        stage('checkout'){
            steps {
                git url:"https://github.com/NiteshBehera/Groovy_test.git" , branch: "main"
            } 
        }
        stage('print line'){
            steps {
              script{
                def data = readFile(file: 'README.md')
                println(data)
              }
            }
        }
        stage('find a word in the file'){
            steps {
                script{
                  import java.io.File
                  def lines = new File(file: 'README.md').readLines()
                  def output = lines.contains('java')
                  println output
                  
                }
            }
        }
    }
}

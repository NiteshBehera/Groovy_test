import java.io.*
import groovy.util.*
import java.util.*
import java.lang.*    
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
                  def lines = new File(file: 'README.md').readLines()
                  def output = lines.contains('java')
                  println output
                  
                }
            }
        }
    }
}

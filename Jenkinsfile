pipeline {
    agent any
    stages {
	
      stage('Clone') {
        steps {
          echo "1.Clone Stage"
          git url: "https://github.com/zhongyuanzhao000/jx-spring.git"
        }
      }
      stage('Package & skip Test') {
        steps {
          echo "2.Package Stage"
	  sh 'source /etc/profile'
          sh 'mvn clean package -DskipTests'
        }
      }
		}
}

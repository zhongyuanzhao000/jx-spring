pipeline {
    agent any
    tools {
        //工具名称必须在Jenkins 管理Jenkins → 全局工具配置中预配置。
        jdk 'jdk'
        maven 'maven-3.6.1'
        
    }
    stages {
	
      stage('Clone') {
        steps {
          echo "Clone..."
                git url: "https://github.com/zhongyuanzhao000/jx-spring.git"
                echo "Clone Successful"
        }
      }
      stage('Package & skip Test') {
        steps {
          echo "Build..."
          sh 'mvn clean package -DskipTests'
          echo "Package Successful"
        }
      }
    }
}

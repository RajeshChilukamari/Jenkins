pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                               
                
                echo "starting ubuntu"
                sh "sudo docker run -d --name=ubuntu ubuntu"
                echo "started ubuntu"
                
                
                
                echo "starting grafana"            
                sh "sudo docker run -d --name=grafana -p 3000:3000 grafana/grafana"
                echo "started grafana"
                
                
                
                echo "starting influxdb"
                sh "sudo docker run -d --name=influxdb -p 8086:8086 influxdb"
                echo "started influxdb"
                
                echo "stoping containers"
                sh "sudo docker stop ubuntu"
                sh "sudo docker stop grafana"
                sh "sudo docker stop influxdb"
                
                echo "removing containers"
                sh "sudo docker rm grafana"
                sh "sudo docker rm ubuntu"
                sh "sudo docker rm influxdb"
            }
        }
    }
}

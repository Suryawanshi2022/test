pipeline{
		agent{
				node{
						label 'Slave-1'
					}
			}
		stages{
		
				stage ('git push'){
						steps{
								sh "yum install httpd -y"
							}
						}
				stage ('apache httpd start'){
						steps{
								sh "service httpd start"
							}
						}
				stage ('deployment of index.html'){
						steps{
								sh "cp -r /mnt/project/test/index.html /var/www/html/"
								sh "chmod -R 777 /var/www/html/index.html"
							}
						}
					}
		}

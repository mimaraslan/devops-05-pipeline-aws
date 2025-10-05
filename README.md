# DevOps Pipeline

## CI/CD Evreni

```

CI/CD:           (Jenkins, Git,  GitHub, GitOps,  GitHub Actions,    GitLab, GitLab CI,    Bitbucket, Bamboo)
Scripting        (Python, Bash, PowerShell)
Containers:      (Docker)
Orchestration:   (Kubernetes, Helm, ArgoCD)
Cloud            (AWS, Azure, GCP)
Virtualization:  (VMware, VirtualBox)
IaC:             (Terraform, Ansible, CloudFormation)
Monitoring:      (Prometheus, Grafana, ELK)
```
<hr>

![AWS DevOps.jpg](public/AWS%20DevOps.jpg)

#### ReactJS - [Next.js](https://nextjs.org) project [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

```bash
npm run dev
```

http://localhost:3000

<hr>

##  1. Makine: Jenkins Master Node

```bash
aws configure
```


```
java --version
docker --version
jenkins --version
trivy --version
sonar-scanner --version
```

### Docker'da tüm containerları listeledik.
```
docker ps -a
```

```
docker stop CONTAINER_ID
docker start CONTAINER_ID

docker ps -a
```

#### SonarQube için Jenkins makinesinin PUBLIC_IP'sini alıp 9000 portuna gideceğiz.

http://PUBLIC_IP:9000


#### React için Jenkins makinesinin PUBLIC_IP'sini alıp 3000 portuna gideceğiz.

http://PUBLIC_IP:3000


#### Jenkins için Jenkins makinesinin PUBLIC_IP'sini alıp 8080 portuna gideceğiz.

http://PUBLIC_IP:8080

```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```






SonarQube aracını Jenkins'e tanıtmak için Token oluşturuyoruz.

http://SONARIN_KURULU_OLDUGU_MAKINENIN_PUBLIC_IP:9000/admin/users



SonarQube aracını Jenkins'e tanıtmak için Token oluşturuyoruz.

http://SONARIN_KURULU_OLDUGU_MAKINENIN_PUBLIC_IP:9000/admin/users


SonarTokenForJenkins
squ_AAAAAAAAAAAA


SonarQubeQualityGates


http://3.233.45.51:9000/admin/webhooks

Create Webhook
http://3.233.45.51:8080/sonarqube-webhook

Proje adı oluşturduk.
Projeye özel webhook oluşturulur.
sonarqube-webhook
http://3.233.45.51:8080/sonarqube-webhook



DockerHub'a gidip Docker Token oluştur.
MyDockerHubTokenForAWS

docker login -u mimaraslan -p  dckr_BBBBBBBBBBB




Jenkins'e DockerHub'ın Token'ınını tanıt.

dockerhub




## ==== 2. Makineyi MontitoringServer Terrafom üzerinden kuracağız.

D:\workspace\devops-2025\devops-05-pipeline-aws\devops-terraform\02_MontitoringServer
içindeki 03_install.sh  prometheus ve node_exporter sürümlerini güncelle
https://github.com/prometheus/prometheus/releases/
https://github.com/prometheus/node_exporter/releases




cd  D:\workspace\devops-2025\devops-05-pipeline-aws\devops-terraform\02_MontitoringServer


Bunu sadece 1 kere yapmamız yeterli. Burada gerek yok.
aws configure



terraform init
terraform plan
terraform apply -auto-approve


Elastic IP aldık.


2. Makineneye MobaXterm üzerinden SSH ile terminalden bağlandık.

Terminale bu komutları yazdık.

sudo systemctl status prometheus
Ctrl+C ile terminalden çık.

sudo systemctl status node_exporter
Ctrl+C ile terminalden çık.

sudo systemctl status grafana-server
Ctrl+C ile terminalden çık.


Prometheus'u URLden çalıştır.
http://MonitoringMakinesinin_PUBLIC_IP:9090



cd /etc/prometheus

sudo nano prometheus.yml

- job_name: "node_exporter"
  static_configs:
    - targets: ["MonitoringMakinesinin_PUBLIC_IP:9090"]




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

![AWS DevOps CI_CD.jpg](public/AWS%20DevOps%20CI_CD.jpg)

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







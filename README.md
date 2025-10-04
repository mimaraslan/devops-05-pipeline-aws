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

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Next.js
First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

<hr>

##  1. Makine: Jenkins Master Node


```
aws configure
```


```
java --version
docker --version
jenkins --version
trivy --version
```

### Docker'da tüm containerları listeledik.
```
docker ps -a

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







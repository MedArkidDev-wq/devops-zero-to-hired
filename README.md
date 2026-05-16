# devops-zero-to-hired

> A structured, honest, 6-month roadmap for engineers with zero DevOps experience to get their first job — built by someone actively doing this journey.

[![Stars](https://img.shields.io/github/stars/MedArkidDev-wq/devops-zero-to-hired?style=social)](https://github.com/MedArkidDev-wq/devops-zero-to-hired)
[![Last Updated](https://img.shields.io/github/last-commit/MedArkidDev-wq/devops-zero-to-hired)]()

> **This is a living document.** I update it as I go through this journey myself. No fluff — only what actually works.

---

## Who Is This For?

- Software/engineering graduates with no DevOps work experience
- Backend developers wanting to transition to infrastructure
- Sysadmins wanting to move into cloud/DevOps
- Anyone told "you need experience to get experience"

---

## The 6-Month Roadmap

### Month 1: Foundations (Do NOT Skip This)

**Goals:**
- [ ] Linux fundamentals (navigation, permissions, processes, networking)
- [ ] Git workflow for infrastructure code
- [ ] AWS Free Tier setup
- [ ] Docker basics — containers, images, Dockerfiles

**Weekly commitment:** 10 hours/week

**Week 1-2: Linux**
```bash
# Practice these until they are muscle memory
ls -la              # List files with details
cd /path/           # Change directory
chmod 755 script.sh # Make executable
chown user:group f  # Change ownership
ps aux              # All running processes
top / htop          # Resource monitor
netstat -tulpn      # Open ports
grep -r "error" /var/log/  # Search file contents
find . -name "*.log"       # Find files
```

**Week 3: Git**
```bash
git init && git branch -M main
git add . && git commit -m "feat: initial commit"
git checkout -b feature/my-change
git push origin feature/my-change
# Open PR -> Review -> Merge -> Delete branch
```

**Week 4: Docker**
```bash
docker build -t my-app .
docker run -d -p 8080:80 my-app
docker compose up -d
docker logs my-app
docker exec -it my-app /bin/sh
```

**Checklist:**
- [ ] Can navigate Linux filesystem confidently
- [ ] Understand file permissions (rwx)
- [ ] Can write and run Bash scripts
- [ ] Have AWS account configured
- [ ] Have first Docker container running
- [ ] Have GitHub profile with SSH key set up

---

### Month 2: Core Infrastructure Tools

**Goals:**
- [ ] Terraform — deploy real AWS infrastructure with code
- [ ] GitHub Actions — your first CI/CD pipeline
- [ ] AWS services — EC2, S3, VPC, IAM
- [ ] AWS Cloud Practitioner exam (attempt)

**Key Skills:**
```bash
# Terraform workflow
terraform init      # Download providers
terraform plan      # Preview changes
terraform apply     # Create resources
terraform destroy   # Delete everything

# GitHub Actions
# Create .github/workflows/ci.yml
# Trigger on push/PR
# Build, test, deploy
```

**Checklist:**
- [ ] Can deploy EC2 + VPC with Terraform
- [ ] Have working GitHub Actions pipeline
- [ ] Understand IAM roles and policies
- [ ] Passed AWS Cloud Practitioner (or scheduled)

---

### Month 3: Container Orchestration + Monitoring

**Goals:**
- [ ] Kubernetes basics — pods, deployments, services
- [ ] Prometheus + Grafana monitoring stack
- [ ] Alerting — what to alert on, how to respond
- [ ] Bash scripting for automation

**Key Skills:**
```bash
# Kubernetes basics
kubectl get pods -n production
kubectl describe pod my-pod
kubectl logs my-pod --previous
kubectl apply -f deployment.yaml
kubectl scale deployment my-app --replicas=3

# Monitoring
docker compose up -d   # Start Prometheus + Grafana
# Import dashboard 1860 (Node Exporter Full)
# Write alert rules for CPU > 80%, disk > 90%
```

**Checklist:**
- [ ] Can deploy apps to Kubernetes
- [ ] Have working monitoring dashboards
- [ ] Can debug CrashLoopBackOff
- [ ] Written first incident post-mortem

---

### Month 4: Production Skills

**Goals:**
- [ ] GitOps with ArgoCD
- [ ] Helm charts
- [ ] Security basics (secrets management, RBAC)
- [ ] AWS Solutions Architect Associate (attempt)

**Key Skills:**
```bash
# ArgoCD
argocd app create my-app --repo URL --path apps/ --dest-server https://kubernetes.default.svc
argocd app sync my-app

# Helm
helm create my-chart
helm install my-app my-chart/ -n production
helm upgrade my-app my-chart/ --set replicas=3
helm rollback my-app 1
```

**Checklist:**
- [ ] Push to Git -> cluster auto-updates (GitOps)
- [ ] Built and published a Helm chart
- [ ] Understand RBAC and secrets
- [ ] Passed SAA (or scheduled)

---

### Month 5: Portfolio + Job Prep

**Goals:**
- [ ] 3 portfolio projects on GitHub (see below)
- [ ] Personal portfolio website
- [ ] LinkedIn optimization
- [ ] First 50 job applications

**Portfolio projects to have:**

| Project | What It Proves |
|---|---|
| [Terraform + CI/CD](https://github.com/MedArkidDev-wq/devops-terraform-cicd) | IaC + automation |
| [Monitoring Stack](https://github.com/MedArkidDev-wq/linux-monitoring-stack) | Observability |
| [Kubernetes GitOps](https://github.com/MedArkidDev-wq/kubernetes-gitops-stack) | K8s + GitOps |

**LinkedIn optimization:**
- Headline: "DevOps Engineer | Terraform | Kubernetes | AWS | CI/CD"
- About: Problem you solve, not list of tools
- Featured: Link to your 3 GitHub projects

---

### Month 6: Active Job Hunt

**Goals:**
- [ ] 100+ applications sent
- [ ] 5+ interviews
- [ ] Job offer

**Application strategy:**
- 15-20 applications per week
- Customize cover letter for each role
- Target "Junior DevOps" and "Cloud Engineer" roles
- Don't ignore "SRE" and "Platform Engineer" titles
- Apply even if you don't meet 100% of requirements

---

## Free Resources (By Topic)

| Topic | Best Free Resource |
|---|---|
| Linux | [Linux Journey](https://linuxjourney.com) |
| Docker | [Play with Docker](https://labs.play-with-docker.com) |
| Kubernetes | [KillerCoda](https://killercoda.com) |
| Terraform | [HashiCorp Learn](https://developer.hashicorp.com/terraform) |
| AWS | [AWS Skill Builder](https://skillbuilder.aws) |
| CI/CD | [GitHub Actions Docs](https://docs.github.com/en/actions) |
| Monitoring | [Grafana Play](https://play.grafana.org) |
| Networking | [Subnetting Practice](https://subnettingpractice.com) |
| Security | [TryHackMe](https://tryhackme.com) |

---

## Certifications Worth Getting

| Certification | Cost | Difficulty | ROI |
|---|---|---|---|
| AWS Cloud Practitioner | $100 | Easy | Good for interviews |
| AWS Solutions Architect Associate | $150 | Medium | Best AWS cert |
| CKA (Certified Kubernetes Admin) | $395 | Hard | Highly valued |
| Terraform Associate | $70 | Medium | Growing demand |
| Linux Foundation Certified SysAdmin | $395 | Medium | Solid foundation |

---

## Contributing

Are you on the same journey? Share what worked for you!
Open a PR with your resource, tip, or experience.

---

**If this roadmap is helping you — please star it!**

## Author

**Mohamed Arkid** — DevOps Engineer and Cloud Consultant

- [moarkid.com](https://moarkid.com)
- [LinkedIn](https://www.linkedin.com/in/mohamed-arkid)

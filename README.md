# DevOps Zero to Hired

A 6-month plan for getting your first DevOps job when you're starting from zero. No bootcamp, no $2000 course. Just the tools, the practice, and the projects.

I'm building this as I go through the process myself. It's not a polished curriculum from someone who got their job 10 years ago. It's what's working right now, updated as I learn what actually matters in interviews and on the job.

## Who this is for

- You finished school and have no DevOps work experience
- You're a developer who wants to move into infrastructure
- You're a sysadmin ready to go cloud-native
- You keep hearing "you need experience to get experience" and it's driving you nuts

## Month 1: Foundations

Learn Linux, Git, and Docker. Don't skip this even if you think you already know it. The interview questions go deeper than you'd expect.

**10 hours/week minimum.**

```bash
# Linux commands that should be muscle memory
ls -la, cd, chmod, chown, ps aux, top, netstat -tulpn
grep -r "error" /var/log/, find . -name "*.log"

# Git workflow
git checkout -b feature/my-change
git add . && git commit -m "feat: add feature"
git push origin feature/my-change
# Open PR -> Review -> Merge

# Docker basics
docker build -t my-app .
docker run -d -p 8080:80 my-app
docker compose up -d
```

By the end of month 1 you should be comfortable navigating Linux, have GitHub set up with SSH, and have your first Docker container running.

## Month 2: Infrastructure as Code

Terraform and GitHub Actions. This is where you start building things that look like real work.

```bash
terraform init && terraform plan && terraform apply
# You just created real AWS infrastructure from code
```

Target the AWS Cloud Practitioner exam this month. It's $100 and it's easy, but it looks good on a resume when you have nothing else.

## Month 3: Kubernetes + Monitoring

Pods, deployments, services. Then set up Prometheus and Grafana so you can actually see what's happening in your cluster.

```bash
kubectl get pods -n production
kubectl logs my-pod --previous    # This one saves you in debugging
kubectl describe pod my-pod       # Look at the Events section
```

Write your first incident post-mortem this month, even if the incident is simulated. Interviewers love seeing that you think about reliability.

## Month 4: Production Skills

ArgoCD (GitOps), Helm charts, RBAC, secrets management. This is the month where your projects start looking like what companies actually run.

Try for the AWS Solutions Architect Associate exam. It's harder than Cloud Practitioner but it's the cert that opens the most doors.

## Month 5: Portfolio + Job Prep

You need 3 projects on GitHub that prove you can do the work:

| Project | What it proves |
|---|---|
| [Terraform + CI/CD](https://github.com/MedArkidDev-wq/devops-terraform-cicd) | You can automate infrastructure |
| [Monitoring Stack](https://github.com/MedArkidDev-wq/linux-monitoring-stack) | You understand observability |
| [Kubernetes GitOps](https://github.com/MedArkidDev-wq/kubernetes-gitops-stack) | You can work with K8s in a real workflow |

Fix your LinkedIn:
- Headline: "DevOps Engineer | Terraform | Kubernetes | AWS | CI/CD"
- About section: Talk about problems you solve, not a list of tools
- Featured section: Link to your 3 GitHub projects

## Month 6: Job Hunt

Send 15-20 applications per week. Don't wait until you feel "ready" because you never will.

Target these titles: Junior DevOps Engineer, Cloud Engineer, SRE, Platform Engineer. Apply even if you don't hit 100% of the requirements. Nobody does.

## Free Resources

| Topic | Best free option |
|---|---|
| Linux | [Linux Journey](https://linuxjourney.com) |
| Docker | [Play with Docker](https://labs.play-with-docker.com) |
| Kubernetes | [KillerCoda](https://killercoda.com) |
| Terraform | [HashiCorp Learn](https://developer.hashicorp.com/terraform) |
| AWS | [AWS Skill Builder](https://skillbuilder.aws) |
| CI/CD | [GitHub Actions docs](https://docs.github.com/en/actions) |
| Monitoring | [Grafana Play](https://play.grafana.org) |

## Certs worth getting

| Cert | Cost | Difficulty |
|---|---|---|
| AWS Cloud Practitioner | $100 | Easy, good for getting past HR filters |
| AWS Solutions Architect Associate | $150 | Medium, best bang for your buck |
| CKA | $395 | Hard, very well respected |
| Terraform Associate | $70 | Medium, growing demand |

## Contributing

If you're on the same path and found something that worked, open a PR.

Star this if it's useful. It helps other people find it.

## About

Built by [Mohamed Arkid](https://moarkid.com). Currently on this journey myself.

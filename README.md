Agustín Maximiliano Álvarez
SysAdmin & Cloud Infrastructure | AWS · Terraform · Docker · Linux | Barcelona

IT professional with years of experience in infrastructure, systems administration, and technical support — actively transitioning into cloud engineering with a focus on AWS.

I build and document real infrastructure from scratch. Two open source projects as evidence:


── build-your-infra ──────────────────────────────────────────

Multi-environment infrastructure lab: local VM, VPS, and AWS Native — built and documented end to end with inline technical reasoning on every decision.

Services deployed (self-managed and AWS managed equivalents, side by side):
- DNS: BIND9 / Route 53 (Private Hosted Zones)
- Web server: Nginx + HTTPS / CloudFront + S3 + ACM
- File transfer: SFTP (OpenSSH hardened) / AWS Transfer Family
- Directory: Samba 4 AD DC + Kerberos / AWS Directory Service
- VPN: WireGuard hub-and-spoke over EC2

AWS stack: EC2 (Graviton2 · ARM64), S3, CloudFront, ACM, Route 53, IAM, VPC, Transfer Family, Directory Service, GuardDuty, CloudTrail, Security Hub, SSM Session Manager, IMDSv2

Linux hardening: UFW, Fail2Ban, AppArmor, auditd, AIDE, rsyslog, sysctl, rkhunter — Lynis score 90 on EC2 / 88 on VM

Automation with Terraform: reusable modules per service + full AWS Native stack in a single terraform apply. Ansible in active implementation for full provisioning from scratch without AMI snapshot dependency.

→ github.com/Bios-Mod/build-your-infra


── containerize-your-infra ───────────────────────────────────

Same infrastructure stack, containerized with Docker — built and documented end to end.

Services deployed:
- DNS: BIND9
- Web server: Nginx
- File transfer: SFTP (atmoz/sftp)
- Reverse proxy + TLS: Traefik v3

Environments: dev (OrbStack / macOS Apple Silicon) and prod (Docker Engine / Ubuntu 24.04 LTS / EC2 ARM64). ARM64-agnostic architecture across both environments.

Automation with Terraform: provisions VPC, subnet, security groups, key pair, and EC2 — user_data installs Docker Engine, clones the repo, and launches the full stack on first boot with zero manual steps on the host.

CI/CD with GitHub Actions: pipelines for Terraform lint/validate, Docker image build, and automated deploy to EC2.

Next: Kubernetes as the natural evolution of the Docker Compose stack.

→ github.com/Bios-Mod/containerize-your-infra


── Stack ─────────────────────────────────────────────────────

AWS          EC2 · S3 · CloudFront · Route 53 · IAM · VPC · GuardDuty · CloudTrail · Transfer Family · Directory Service · SSM
IaC          Terraform (modules · remote state S3+DynamoDB · user_data · multi-module stacks)
Containers   Docker Engine · Docker Compose v2 · Traefik v3 · Nginx · BIND9 · SFTP
CI/CD        GitHub Actions
Linux        Ubuntu Server 24.04 LTS · ARM64 + x86_64 · systemd · Netplan
Security     UFW · Fail2Ban · AppArmor · auditd · AIDE · WireGuard · CIS Benchmark L1
Scripting    Bash · Git
Next         Ansible · Kubernetes


── Certifications ────────────────────────────────────────────

- AWS Cloud Practitioner — May 2026
- Google IT Support Professional — April 2026
- Higher Technician in IT Infrastructure Systems Support — Argentina, 2019
- Preparing: AWS Solutions Architect Associate


── Contact ───────────────────────────────────────────────────

LinkedIn → linkedin.com/in/agustin-maximiliano-alvarez
Location → Montcada i Reixac, Barcelona · Open to hybrid / remote
Languages → Spanish (native) · English (B1/B2) · Catalan (functional)

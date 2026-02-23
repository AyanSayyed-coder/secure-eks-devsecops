# Secure EKS DevSecOps Project

This project demonstrates a production-grade secure CI/CD pipeline on Amazon EKS using:

- GitHub OIDC Authentication
- IAM Roles for Service Accounts (IRSA)
- HashiCorp Vault for dynamic secrets
- Zero static AWS credentials
- Least privilege IAM policies

## Architecture

GitHub Actions → OIDC → AWS IAM → EKS  
Pods → IRSA → Vault → Dynamic Secrets

## Status

Phase 1: Infrastructure Setup ✅  
Phase 2: IAM & Identity (In Progress)
rbac-fix

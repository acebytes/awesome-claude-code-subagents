# Terraform Engineer

Expert Terraform engineer specializing in infrastructure as code, multi-cloud provisioning, and modular architecture. Masters Terraform best practices, state management, and enterprise patterns with focus on reusability, security, and automation.

## Overview

The Terraform Engineer agent is a senior-level infrastructure specialist that helps design, implement, and maintain enterprise-grade infrastructure as code using Terraform. This agent excels at creating reusable modules, managing complex state configurations, ensuring security compliance, and integrating Terraform workflows into CI/CD pipelines across AWS, Azure, and GCP.

## Key Capabilities

- **Infrastructure as Code**: Design and implement scalable, maintainable Terraform code
- **Multi-Cloud Provisioning**: Expert-level knowledge of AWS, Azure, and GCP providers
- **Modular Architecture**: Create reusable, composable modules with >80% reusability
- **State Management**: Robust remote backends, locking, and disaster recovery strategies
- **Security Compliance**: Policy as code, compliance scanning, and security best practices
- **Cost Optimization**: Cost estimation, tracking, and FinOps integration
- **CI/CD Integration**: Automated plan/apply workflows with approval gates
- **Testing**: Comprehensive unit, integration, and compliance testing strategies

## Slash Commands

### /tf-module
Create a new Terraform module following best practices with proper structure, validation, and documentation.

**Example:**
```
/tf-module vpc-network
```

Creates a VPC network module with:
- Input validation
- Output contracts
- Provider configuration
- Resource tagging
- Complete documentation

### /tf-plan
Generate and analyze a Terraform execution plan with security and cost implications.

**Example:**
```
/tf-plan production
```

Generates plan with:
- Resource change summary
- Security impact analysis
- Cost estimation
- Compliance checks
- Risk assessment

### /tf-migrate
Migrate existing infrastructure to Terraform or between different state backends.

**Example:**
```
/tf-migrate aws-resources
```

Handles:
- Resource import strategies
- State file migration
- Backend reconfiguration
- Validation testing
- Rollback procedures

## MCP Servers

### filesystem
Provides access to local filesystem for reading and writing Terraform files, modules, and configurations.

### github
Integrates with GitHub for managing Terraform repositories, pull requests, and collaborative workflows.

### context7
Accesses comprehensive Terraform documentation and provider-specific best practices.

## Use Cases

### 1. Module Development
Create reusable, well-documented Terraform modules:
- Composable architecture design
- Input validation and type constraints
- Output contract definitions
- Version constraints and dependencies
- Provider configuration patterns

### 2. State Management
Implement robust state management strategies:
- Remote backend configuration (S3, Azure Blob, GCS)
- State locking with DynamoDB or equivalent
- Workspace strategies for multi-environment
- State migration and import workflows
- Disaster recovery procedures

### 3. Multi-Environment Workflows
Manage infrastructure across environments:
- Environment isolation strategies
- Variable and secret management
- DRY configuration patterns
- Promotion pipelines
- Drift detection and remediation

### 4. Security Compliance
Ensure infrastructure meets security standards:
- Policy as code implementation
- Automated compliance scanning
- Secret management integration (Vault, AWS Secrets Manager)
- IAM least privilege principles
- Network security patterns

### 5. Cost Management
Track and optimize infrastructure costs:
- Pre-deployment cost estimation
- Resource tagging for cost allocation
- Usage tracking and optimization
- Waste identification
- Chargeback and FinOps integration

### 6. CI/CD Integration
Automate Terraform workflows:
- Pipeline automation (GitLab CI, GitHub Actions, Jenkins)
- Plan/apply workflow automation
- Approval gates and RBAC
- Automated testing and validation
- Security and cost scanning

## Terraform Engineering Checklist

The agent ensures these standards are met:
- Module reusability >80% achieved
- State locking enabled consistently
- Plan approval required always
- Security scanning passed completely
- Cost tracking enabled throughout
- Documentation complete automatically
- Version pinning enforced strictly
- Testing coverage comprehensive

## Provider Expertise

### AWS
- VPC networking and security groups
- EC2, ECS, EKS orchestration
- S3, RDS, DynamoDB data services
- IAM roles and policies
- Lambda and serverless

### Azure
- Virtual networks and NSGs
- VM scale sets and AKS
- Storage accounts and SQL databases
- Azure AD and RBAC
- Azure Functions

### GCP
- VPC networks and firewall rules
- Compute Engine and GKE
- Cloud Storage and Cloud SQL
- IAM and service accounts
- Cloud Functions

### Additional Providers
- Kubernetes provider
- Helm provider
- Vault provider
- Custom provider development

## Best Practices

### Module Design
- Keep modules small and focused
- Use semantic versioning
- Implement input validation
- Follow naming conventions
- Tag all resources
- Document thoroughly

### State Management
- Always use remote backends
- Enable state locking
- Encrypt state files
- Regular backups
- Test disaster recovery

### Security
- Never commit secrets
- Use data sources for sensitive data
- Implement least privilege IAM
- Enable audit logging
- Regular security scanning

### Testing
- Unit test modules
- Integration test deployments
- Compliance validation
- Cost testing
- End-to-end scenarios

## Integration with Other Agents

The Terraform Engineer works seamlessly with:
- **cloud-architect**: Implement architectural designs with IaC
- **devops-engineer**: Automate infrastructure provisioning
- **security-engineer**: Implement secure infrastructure patterns
- **kubernetes-specialist**: Provision and manage K8s clusters
- **platform-engineer**: Build platform infrastructure
- **sre-engineer**: Implement reliability patterns
- **network-engineer**: Design and implement network infrastructure
- **database-administrator**: Provision and configure databases

## Getting Started

1. **Initialize Agent**: Load the Terraform Engineer with MCP servers configured
2. **Assess Infrastructure**: Agent reviews existing Terraform code and requirements
3. **Plan Implementation**: Design module architecture and state strategy
4. **Execute**: Create modules, implement state management, set up CI/CD
5. **Validate**: Run tests, security scans, and cost analysis
6. **Document**: Generate comprehensive documentation
7. **Train**: Knowledge transfer to team members

## Example Workflows

### Creating a New Module
```
User: Create a production-ready VPC module for AWS
Agent: /tf-module aws-vpc
- Analyzes requirements
- Creates module structure
- Implements validation
- Adds documentation
- Writes tests
```

### Migrating Infrastructure
```
User: Migrate our existing AWS resources to Terraform
Agent: /tf-migrate aws-production
- Inventories resources
- Creates import scripts
- Generates Terraform code
- Validates configuration
- Documents changes
```

### Planning Deployment
```
User: Generate plan for production deployment
Agent: /tf-plan production
- Runs terraform plan
- Analyzes changes
- Estimates costs
- Checks security
- Provides recommendations
```

## Requirements

- Terraform 1.0+
- Cloud provider CLI tools (AWS CLI, Azure CLI, gcloud)
- Git for version control
- MCP servers configured (filesystem, github, context7)

## Advanced Features

- Dynamic block generation
- Complex conditional logic
- Meta-argument patterns (count, for_each, depends_on)
- Provider aliases for multi-region/multi-account
- Module composition patterns
- Data source optimization
- Custom function development

## Support

For questions, issues, or contributions, please refer to the main marketplace repository.

## License

MIT License - See LICENSE file for details

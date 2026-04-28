---
copyright: dbj dot org
year: 2025
---

# Primordial DBJ Method Workflow

## Workflow Terminology

**Roles**

| Role | Responsibilities |
|------|-----------------|
| Business Owner | - Defines functional requirements<br>- Sets module boundaries<br>- Approves final specifications |
| Business Analyst | - Details requirements<br>- Validates specifications<br>- Coordinates between teams |
| System Architect | - Ensures technical feasibility<br>- Reviews system integrity<br>- Approves technical designs |
| IT Team | - Implements modules<br>- Maintains systems<br>- Handles deployments |

### Actions

#### Business Actions
- **Define**: Create new module specifications
- **Update**: Modify existing module features
- **Remove**: Deprecate and remove modules

#### Technical Actions
- **Validate**: Review and approve specifications
- **Implement**: Develop module features
- **Deploy**: Release to production environment

## Workflow Patterns

### Module Creation Flow

```mermaid
sequenceDiagram
    participant BO as Business Owner
    participant BA as Business Analyst
    participant SA as System Architect
    participant IT as IT Team

    BO->>BA: Define new module
    BA->>SA: Validate specifications
    SA->>BA: Technical feedback
    BA->>BO: Request clarifications
    BO->>BA: Provide clarifications
    BA->>SA: Update specifications
    SA->>IT: Approve implementation
    IT->>SA: Complete development
    SA->>BA: Validate implementation
    BA->>BO: Sign off deployment
    IT->>IT: Deploy module
```

### Change Management

```mermaid
graph TD
subgraph IT[IT]
I[Implementation]
end
subgraph BIT[Business & IT]
G[Review Cycle]
end
    A[Identify Change] --> B{Change Type}
    B -->|Trivial| C[Update Feature]
    B -->|Non-trivial| D[Module Change]
    D --> F[Specification Update]
    C --> F
    F --> BIT
    BIT --> IT
    %% I --> M[Maintenance]
```

## Best Practices

1. **Clear Communication**
   - Common vocabulary
   - Document all decisions
   - Standardize and template
   - Maintain change logs

2. **Version Control**
   - Track specification versions
   - Document API changes
   - Maintain migration paths

3. **Quality Assurance**
   - Regular validation cycles
   - Automated testing
   - Performance monitoring


---
![alt text](assests/dbj-org-logo-64.jpg)
> &copy; dbj dot org ltd 
> 
> CC BY SA 4.0
# Example Use Case: E-commerce Platform

This example demonstrates how to use the full-stack dev team prompts to build a complete e-commerce platform.

## Project Overview

**Goal**: Build a modern, scalable e-commerce platform with customer portal, admin dashboard, and mobile app.

**Target Users**:
- Customers: Browse products, make purchases, track orders
- Administrators: Manage inventory, process orders, view analytics
- Vendors: List products, manage inventory, view sales

**Key Features**:
- Product catalog with search and filters
- Shopping cart and checkout
- Payment processing (Stripe/PayPal)
- Order management and tracking
- User authentication and profiles
- Admin dashboard
- Mobile applications (iOS/Android)

## Team Workflow

### Phase 1: Planning & Architecture (Weeks 1-2)

#### 1. Product Manager
**Prompt**: Use `/prompts/product-manager/product-owner.md`

**Input**:
```
I am building an e-commerce platform for small to medium-sized businesses.

Target Users: B2C consumers, age 25-45, tech-savvy
Business Goals: 
- Enable businesses to sell online with minimal setup
- Provide seamless customer experience
- Support multiple payment methods
- Mobile-first approach

Current State: No existing system
Desired State: Full-featured e-commerce platform with web and mobile apps

Questions:
1. What user stories should be created for MVP?
2. How should features be prioritized?
3. What are the acceptance criteria?
```

**Output**: User stories, feature prioritization, MVP scope, success metrics

#### 2. Tech Lead/Architect
**Prompt**: Use `/prompts/tech-lead/solution-architect.md`

**Input**:
```
I am building an e-commerce platform.

Technical Context:
- Expected 10,000+ daily active users
- Performance: Page load < 2s, API response < 500ms
- Technology Stack: Node.js/TypeScript, React, PostgreSQL
- Cloud Platform: Azure
- Team: 5 developers (2 frontend, 2 backend, 1 full-stack)

Functional Requirements:
- Product catalog (search, filter, sort)
- Shopping cart and checkout
- Order management
- Payment processing
- User authentication
- Admin dashboard

Non-Functional Requirements:
- Performance: 1000 concurrent users
- Security: PCI DSS compliance for payments
- Scalability: 10x growth in 1 year
- Availability: 99.9% uptime

Questions:
1. What architecture pattern should we use?
2. How should we structure the application?
3. What are the key technical decisions?
```

**Output**: System architecture, ADRs, technology stack, data flow diagrams

### Phase 2: Design (Weeks 2-4)

#### 3. UI/UX Designer
**Prompt**: Use `/prompts/ui-ux/ui-ux-designer.md`

**Input**:
```
I need UI/UX design for an e-commerce platform.

Project Context:
- Product Type: Web app + Mobile app
- Target Users: Consumers age 25-45, primarily mobile users
- Business Goals: High conversion rate, low cart abandonment
- Brand: Modern, clean, trustworthy

User Requirements:
- Quick product discovery
- Easy checkout process (< 3 steps)
- Mobile-optimized experience
- Accessibility: WCAG 2.1 AA

Design Requirements:
- Mobile-first design
- Modern, clean aesthetic
- Trust signals (security badges, reviews)
- Fast loading indicators

Questions:
1. What should the checkout flow be?
2. How should I organize the product catalog?
3. What's the best mobile navigation pattern?
```

**Output**: Wireframes, high-fidelity mockups, design system, user flows

### Phase 3: Development (Weeks 4-12)

#### 4. Backend Developer
**Prompt**: Use `/prompts/backend-dev/backend-developer.md`

**Input**:
```
I need to build REST APIs for an e-commerce platform.

Technical Requirements:
- Language/Runtime: Node.js with TypeScript
- Framework: NestJS
- Database: PostgreSQL
- Caching: Redis
- Authentication: JWT
- API Style: REST

Functional Requirements:
- Product CRUD operations
- Shopping cart management
- Order processing
- User authentication
- Payment integration (Stripe)
- Inventory management

Data Model:
- Users, Products, Categories, Orders, OrderItems, Cart, Payments

Non-Functional Requirements:
- Performance: 500ms API response time
- Security: OWASP Top 10, PCI DSS
- Scalability: 1000 concurrent requests

Questions:
1. How should I structure the cart API?
2. What's the best approach for inventory management?
3. How do I handle payment processing securely?
```

**Output**: API endpoints, database schema, business logic, tests

#### 5. Frontend Developer
**Prompt**: Use `/prompts/frontend-dev/frontend-developer.md`

**Input**:
```
I need to build the customer-facing e-commerce web application.

Technical Requirements:
- Framework: React with TypeScript
- State Management: Redux Toolkit + RTK Query
- Styling: Tailwind CSS
- UI Library: Headless UI

Functional Requirements:
- Product listing with search/filter
- Product detail pages
- Shopping cart
- Checkout flow
- User authentication
- Order history

Design Requirements:
- Responsive: Mobile/Tablet/Desktop
- Accessibility: WCAG 2.1 AA
- Browser Support: Chrome, Firefox, Safari, Edge (latest 2 versions)
- Performance: Lighthouse score 90+

Questions:
1. How should I structure the cart state?
2. What's the best approach for the checkout flow?
3. How do I optimize for performance?
```

**Output**: React components, state management, API integration, tests

#### 6. Database Engineer
**Prompt**: Use `/prompts/database/database-engineer.md`

**Input**:
```
I need database design for an e-commerce platform.

Technical Context:
- Database: PostgreSQL 14
- Expected Data Volume: 100K products, 1M users, 10M orders
- Read/Write Ratio: 70% read, 30% write
- Performance: Query response < 100ms

Data Requirements:
- Entities: Users, Products, Categories, Orders, OrderItems, Cart, Reviews, Inventory
- Relationships: Products belong to Categories, Orders have OrderItems, etc.

Performance Requirements:
- Product search: < 100ms
- Checkout: < 500ms
- Analytics queries: < 5s

Questions:
1. How should I structure the schema for optimal performance?
2. What indexes should I create?
3. How do I handle inventory tracking?
```

**Output**: Database schema, indexes, queries, migration scripts

### Phase 4: DevOps & Infrastructure (Weeks 8-10)

#### 7. DevOps Engineer
**Prompt**: Use `/prompts/devops/devops-engineer.md`

**Input**:
```
I need to set up CI/CD and infrastructure for an e-commerce platform on Azure.

Technical Context:
- Cloud Platform: Azure
- Application: Node.js backend, React frontend
- Database: PostgreSQL
- Team: 5 developers

Infrastructure Requirements:
- Environment: Dev, Staging, Production
- Compute: Containers (Docker)
- Database: Azure Database for PostgreSQL
- Storage: Azure Blob Storage
- CDN: Azure Front Door

CI/CD Requirements:
- Source Control: GitHub
- Build: On every PR
- Testing: Unit, integration, E2E tests
- Deployment: Blue-green deployment
- Environments: Auto-deploy to dev, manual approve for prod

Questions:
1. How should I structure the CI/CD pipeline?
2. What infrastructure components do I need?
3. How do I implement blue-green deployment?
```

**Output**: Infrastructure as Code, CI/CD pipelines, deployment procedures

#### 8. Cloud/Azure Specialist
**Prompt**: Use `/prompts/cloud-azure/azure-specialist.md`

**Input**:
```
I need Azure architecture for an e-commerce platform.

Project Context:
- Application Type: Web app with API backend
- Current State: New project
- Technology: Node.js, React, PostgreSQL
- Team: 5 developers, moderate Azure experience

Requirements:
- Compute: Web app hosting, API hosting
- Data: PostgreSQL database, Redis cache, Blob storage
- Integration: Payment gateway (Stripe), Email service
- Security: PCI DSS compliance, Azure AD authentication
- Scale: 10,000 daily users, 100K products

Non-Functional:
- Availability: 99.9% uptime
- Performance: < 2s page load, < 500ms API response
- Scalability: Auto-scale to handle traffic spikes
- Cost: $2,000-3,000/month budget

Questions:
1. What Azure services should I use?
2. How do I architect for PCI DSS compliance?
3. What's the cost optimization strategy?
```

**Output**: Azure architecture diagram, service selection, cost estimates

### Phase 5: Security & Quality (Ongoing)

#### 9. Security Engineer
**Prompt**: Use `/prompts/security/security-engineer.md`

**Input**:
```
I need security assessment for an e-commerce platform.

Technical Context:
- Application: E-commerce web app
- Tech Stack: Node.js, React, PostgreSQL, Azure
- Data Sensitivity: PII, payment data (credit cards)
- Current State: In development

Security Requirements:
- Authentication: User login with 2FA
- Authorization: RBAC (customer, admin, vendor)
- Data Protection: Encrypt PII, tokenize payment data
- Compliance: PCI DSS, GDPR
- Audit Logging: All financial transactions

Questions:
1. What security vulnerabilities should I address?
2. How do I achieve PCI DSS compliance?
3. What authentication strategy should I use?
```

**Output**: Security assessment, authentication implementation, compliance checklist

#### 10. QA/Testing Engineer
**Prompt**: Use `/prompts/qa-testing/qa-engineer.md`

**Input**:
```
I need comprehensive testing strategy for an e-commerce platform.

Technical Context:
- Application: Web app (React frontend, Node.js backend)
- Tech Stack: React, NestJS, PostgreSQL
- Current Coverage: 60% code coverage
- CI/CD: GitHub Actions

Functional Requirements:
- Product search and filtering
- Shopping cart operations
- Checkout and payment flow
- Order management
- User authentication

Quality Requirements:
- Test Coverage: 80%+ code coverage
- Performance: Load testing for 1000 concurrent users
- Browser Support: Chrome, Firefox, Safari, Edge
- Accessibility: WCAG 2.1 AA

Questions:
1. What test cases should be created for checkout?
2. How should I structure the E2E tests?
3. What performance testing approach should I use?
```

**Output**: Test strategy, test cases, automated tests, performance tests

## Expected Deliverables

### Documentation
- [x] Product requirements document (PRD)
- [x] User stories and acceptance criteria
- [x] System architecture diagrams
- [x] API documentation (OpenAPI/Swagger)
- [x] Database schema and ER diagrams
- [x] Design system and style guide
- [x] Deployment runbooks
- [x] Security documentation

### Code & Infrastructure
- [x] Backend APIs (Node.js/NestJS)
- [x] Frontend application (React)
- [x] Database migrations
- [x] Infrastructure as Code (Bicep/Terraform)
- [x] CI/CD pipelines (GitHub Actions)
- [x] Docker configurations
- [x] Kubernetes manifests (if applicable)

### Testing
- [x] Unit tests (80%+ coverage)
- [x] Integration tests
- [x] E2E tests (Cypress/Playwright)
- [x] Performance tests (k6)
- [x] Security tests (OWASP ZAP)
- [x] Accessibility tests

### Monitoring
- [x] Application Insights instrumentation
- [x] Log Analytics queries
- [x] Alert rules
- [x] Dashboards
- [x] Cost monitoring

## Success Metrics

### Technical Metrics
- **Performance**: Page load time < 2s, API response < 500ms
- **Reliability**: 99.9% uptime
- **Test Coverage**: 80%+ code coverage
- **Security**: Zero critical vulnerabilities
- **Accessibility**: WCAG 2.1 AA compliance

### Business Metrics
- **Conversion Rate**: 3%+ (industry average: 2-3%)
- **Cart Abandonment**: < 70% (industry average: 70%)
- **Customer Satisfaction**: 4.5+/5.0
- **Time to Purchase**: < 5 minutes
- **Mobile Traffic**: 60%+ of total traffic

## Timeline

- **Week 1-2**: Planning and architecture
- **Week 2-4**: Design and prototyping
- **Week 4-12**: Development (iterative sprints)
- **Week 8-10**: Infrastructure and DevOps setup
- **Week 10-14**: Testing and QA
- **Week 14-16**: Security audit and compliance
- **Week 16**: Production deployment
- **Week 16+**: Monitoring, optimization, iteration

## Tips for Using This Example

1. **Start with Product Manager**: Define clear requirements before technical work
2. **Architecture First**: Get Tech Lead input before starting development
3. **Design Early**: UI/UX design should inform frontend development
4. **Parallel Development**: Frontend and Backend can develop concurrently with agreed API contracts
5. **Continuous Testing**: QA should be involved from sprint 1
6. **Security Review**: Security Engineer should review architecture and code regularly
7. **DevOps from Day 1**: Set up CI/CD early to enable rapid iteration
8. **Cloud Early**: Provision cloud infrastructure early to test integrations

## Common Pitfalls to Avoid

❌ **Skipping Architecture**: Starting to code without clear architecture leads to refactoring
❌ **No API Contract**: Frontend and Backend must agree on API contracts upfront
❌ **Ignoring Security**: Security is easier to build in than bolt on later
❌ **Manual Deployments**: Automate deployments from the start
❌ **No Monitoring**: Set up monitoring before launch, not after issues arise
❌ **Over-Engineering**: Build for current needs, not hypothetical future scale
❌ **Skipping Tests**: Tests save time in the long run
❌ **Ignoring Accessibility**: Accessibility is a requirement, not a nice-to-have

## Next Steps

After completing this project, consider:
- Mobile app development (React Native or native iOS/Android)
- Advanced analytics and reporting
- AI-powered product recommendations
- Multi-vendor marketplace features
- International expansion (i18n, multi-currency)
- Advanced inventory management
- Customer loyalty programs

---

**Version**: 1.0  
**Last Updated**: 2025-01  
**Maintained By**: Prompts-FullStackDevTeam

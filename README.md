# OWASP Top 10 for LLMs: Same Threats, New Vectors

## Presentation Overview

This repository contains resources for the conference presentation "Same Threats - New Vectors: OWASP Top 10 for LLMs" delivered at AI in Production 2025.

**Presenter:** David Hawthorne  
**Website:** [davidhawthorne.com](https://davidhawthorne.com)  
**Focus Areas:** Data Engineering, ML/Analytics, Cloud Architecture, Security & Compliance (SOC 2, GDPR, PDPA)

## Abstract

LLMs inherit familiar web-era risks with new vulnerabilities. This session maps OWASP's Top 10 for LLMs to the OWASP Top 10 for web applications, offering practical security insights for product leaders, managers, developers, and cybersecurity professionals. By understanding how they are related we can effectively eliminate risks.

## Three Core Themes from the Talk

### 1. Input & Data Security
Understanding how unvalidated inputs, weak boundaries, and data integrity issues can lead to prompt injection, adversarial manipulation, and sensitive data exposure.

### 2. Asset Protection & Abuse Prevention  
Defending against model misuse, API exploitation, and system compromise through effective access controls and protection strategies.

###  3. Trust, Governance & Transparency
Building resilient system design, strong observability, and governance structures for responsible AI usage.

## OWASP Resources

### Official OWASP LLM Documentation
- **[OWASP Top 10 for LLMs 2025](https://genai.owasp.org/llm-top-10/)** - The official 2025 list
- **[OWASP GenAI Security Project](https://genai.owasp.org/)** - Main project page
- **[OWASP Red Teaming Guide for LLMs](https://genai.owasp.org/resource/red-teaming-guide/)** - Comprehensive testing methodology

### OWASP for Web Application Security
- **[OWASP Top 10](https://owasp.org/Top10/)** - Web application security risks
- **[OWASP Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)** - Security testing methodology

## Security Tools, Platforms, etc.

### Evaluation Driven Development (EDD): TDD for the AI Era

**Core Concept:** Extend Test Driven Development principles to AI systems with continuous evaluation throughout the development lifecycle.

**Traditional TDD:** Red → Green → Refactor  
**AI EDD:** Evaluate → Build → Test → Deploy → Monitor

**Key Differences:**
- **TDD Focus:** Does the code work as intended?
- **EDD Focus:** Does the AI behave safely, fairly, and reliably?

**Business Value:** EDD catches AI failures before customers experience them, preventing the PR disasters, bias, and other issues.

### AI Evaluation & Testing Frameworks
- **[DeepEval](https://github.com/confident-ai/deepeval)** - LLM evaluation framework with unit testing capabilities and multiple output metrics
- **[CyberSecEval](https://ai.meta.com/research/publications/cyberseceval-3-advancing-the-evaluation-of-cybersecurity-risks-and-capabilities-in-large-language-models/)** - Meta's benchmark for quantifying LLM security risks and capabilities
- **[HarmBench](https://arxiv.org/abs/2402.04249)** - Standardized evaluation framework for automated red teaming and robust refusal
- **[JailbreakBench](https://arxiv.org/abs/2404.01318)** - Open robustness benchmark for jailbreaking large language models
- **[PyRIT](https://github.com/Azure/PyRIT)** - Microsoft AI Red Team toolkit for LLM endpoint assessment
- **[Promptfoo](https://github.com/promptfoo/promptfoo)** - Red teaming, pen testing and vulnerability scanning for LLMs
- **[MoonShot](https://github.com/aiverify-foundation/moonshot)** - Simple and modular tool to evaluate any LLM application

### Advanced Evaluation Tools
- **[Dioptra](https://pages.nist.gov/dioptra/)** - NIST software test platform for assessing AI trustworthy characteristics
- **[ModelScan](https://github.com/protectai/modelscan)** - Detect various types of model serialization attacks
- **[LLM Attacks](https://llm-attacks.org/)** - Automatic construction of adversarial attacks on LLMs
- **[StrongREJECT](https://arxiv.org/abs/2402.10260)** - Jailbreak benchmark with valuation methodology

### Prompt Injection Protection
- **[LLM Guard](https://llm-guard.com/)** - Open-source prompt injection detection (4.1M+ downloads)
- **[Prompt Security](https://promptsecurity.com/)** - Commercial platform for sophisticated injection detection  
- **[Lakera Guard](https://www.lakera.ai/guard)** - AI security API for real-time protection

### Data Protection & PII Detection
- **[Protecto](https://protecto.ai/)** - AI-powered PII/PHI detection with 99% accuracy preservation
- **[Microsoft Presidio](https://github.com/microsoft/presidio)** - Open-source PII anonymization framework

### Vector Database Security
- **[IronCore Cloaked AI](https://ironcorelabs.com/cloaked-ai/)** - Application-layer encryption for vector databases
- **[Enkrypt AI](https://enkryptai.com/)** - RAG security platform for secure vector search
- **[OpenSearch Security](https://opensearch.org/docs/latest/security/)** - Built-in access controls and monitoring

### Agent & Output Validation
- **[Guardrails AI](https://guardrailsai.com/)** - Agent output validation and action restrictions
- **[Robust Intelligence](https://www.robustintelligence.com/)** - AI firewall with misinformation detection
- **[Scale AI](https://scale.com/)** - Human-in-the-loop systems for output verification

### Supply Chain Security
- **[CycloneDX](https://cyclonedx.org/)** - OWASP's project to create ML SBOMs
- **[CycloneDX SBOM Utility](https://github.com/CycloneDX/sbom-utility)** - CLI tool for validating model integrity in CI/CD
- **[ModelScan](https://github.com/protectai/modelscan)** - Open-source tool to scan ML models for malicious payloads

### Cost & Consumption Monitoring
- **[Langfuse](https://langfuse.com/)** - Token usage analytics and consumption tracking
- **[LangSmith](https://smith.langchain.com/)** - LLM application observability platform
- **[AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/)** - Cloud cost monitoring and alerts
- **[Azure Cost Management](https://azure.microsoft.com/en-us/products/cost-management/)** - Azure cost monitoring and optimization

### Rate Limiting & Circuit Breakers
- **[Nginx](https://www.nginx.com/)** - Web server with built-in rate limiting
- **[Cloudflare](https://www.cloudflare.com/)** - CDN and DDoS protection with rate limiting
- **[AWS API Gateway](https://aws.amazon.com/api-gateway/)** - API management with throttling
- **[Hystrix](https://github.com/Netflix/Hystrix)** - Latency and fault tolerance library
- **[resilience4j](https://resilience4j.readme.io/)** - Fault tolerance library for Java applications

## Security Frameworks Presented

### Strategic Security Assessment Framework

1. **Inventory Assets** - items and categories might include: customer-facing and internal tools, data pipelines, RAG context, etc. know their contents and locations.
2. **Strategic Decisions** - Risk assessment questions:
   - Can this destroy my business if compromised?
   - Does it access sensitive data?
   - Does it take actions?
   - Is it revenue generating?
   - How would I explain this to customers?
3. **Risk-Impact Matrix** - Prioritization strategy:
   - High Risk + High Impact: Immediate intervention
   - Low Risk + High Impact: Monitor closely  
   - Low Risk + Low Impact: Standard controls sufficient
4. **Implementation** - Apply controls and monitor

### Sarah's Contributions (Technical)

- **Risk Assessment** - What could go wrong, how do we test each feature?
- **Human Oversight** - AI assists, humans decide (bake into products and agents)
- **Output Validation** - Never publish AI content without review
- **Incident Response** - Clear escalation paths when AI fails
- **Evaluation Driven Development** - Integrate continuous AI evaluation into development culture

### Marcus's Contributions (Strategic)

- **Foundational** - Data quality and bias detection
- **Validation** - AI assists, humans decide (embedded in products/agents)
- **Transparency** - Explainable decisions and audit trails, compliance
- **Governance** - Clear policies and accountability for teams

## OWASP Top 10 for LLMs (2025) Quick Reference

| # | LLM Vulnerability | Sample Web Related/Underneath |
|---|---|---|
| LLM01 | Prompt Injection | A03:2021 - Injection |
| LLM02 | Sensitive Information Disclosure | A01:2021 - Broken Access Control |
| LLM03 | Supply Chain Vulnerabilities | A06:2021 - Vulnerable Components |
| LLM04 | Data and Model Poisoning | A03:2021 - Injection |
| LLM05 | Improper Output Handling | A08:2021 - Software Integrity Failures |
| LLM06 | Excessive Agency | A04:2021 - Insecure Design |
| LLM07 | System Prompt Leakage | A05:2021 - Security Misconfiguration |
| LLM08 | Vector and Embedding Weaknesses | A01:2021 - Broken Access Control |
| LLM09 | Misinformation | A04:2021 - Insecure Design |
| LLM10 | Unbounded Consumption | A04:2021 - Insecure Design |

## Key Takeaways

1. **Same Principles, New Systems** - Traditional security principles apply to AI systems with new attack vectors
2. **AI Security is Business Strategy** - Security failures cascade into strategic business problems  
3. **Trust Through Transparency** - Build accountable AI through layered governance, not perfect AI
4. **Treat AI Like Privileged Applications** - Apply the same rigor you use for business-critical systems
5. **Evaluation Driven Development** - Extend TDD principles to AI systems for continuous safety and reliability assessment

## Additional Resources

### Evaluation
- **[AI Evaluation post by Mauzma Zahid](https://www.linkedin.com/posts/muazmazahid_learnwithmz-ai-productmanagement-activity-7339338076504150016-2k0b?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAHPCPABvEmoD-kUsIMMiDwv72zC7xlcsGc)** "As AI features become core to product roadmaps, evaluating AI systems is no longer just a research problem. It's a product responsibility. Whether you're building copilots, agents, search, or agentic systems, you need to know how to measure what "good" looks like."

### Academic & Research
- **[NIST: There's more to bias than biased data](https://www.nist.gov/news-events/news/2022/03/theres-more-ai-bias-biased-data-nist-report-highlights)** - Rooting out bias in artificial intelligence will require addressing human and systemic biases as well.
- **[TruthfulQA](https://github.com/sylinrl/TruthfulQA)** - Benchmark for measuring model truthfulness
- **[AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)** - NIST AI RMF 1.0

### Industry Standards & Compliance
- **[ISO/IEC 27001](https://www.iso.org/isoiec-27001-information-security.html)** - Information security management
- **[SOC 2](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/aicpasoc2report)** - Security, availability, and confidentiality
- **[EU AI Act](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52021PC0206)** - European AI regulation

### Secret Management
- **[Azure Key Vault](https://azure.microsoft.com/en-us/products/key-vault/)** - Cloud secret management
- **[AWS Secrets Manager](https://aws.amazon.com/secrets-manager/)** - AWS secret management service
- **[HashiCorp Vault](https://www.vaultproject.io/)** - Multi-cloud secret management

## Contact Information

**David Hawthorne**  
Director of Cloud Engineering, O3 Solutions  
Website: [davidhawthorne.com](https://davidhawthorne.com)  
LinkedIn: [Connect on LinkedIn](https://linkedin.com/in/davidhawthorne)  


## License & Usage

This presentation and associated materials are shared for educational purposes. All opinions are my own and not of my employer.
---

*"Security isn't just about preventing attacks - it's about enabling sustainable innovation."*
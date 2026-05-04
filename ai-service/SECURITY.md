# Security Threats — AI Service

## Threat 1: Prompt Injection
- Description: Attacker manipulates AI prompts to bypass security
- Risk: High
- Mitigation: Input sanitisation, injection pattern detection

## Threat 2: API Key Exposure
- Description: Groq API key accidentally committed to GitHub
- Risk: High
- Mitigation: Store in .env file, .env added to .gitignore

## Threat 3: Rate Limit Abuse
- Description: Attacker floods endpoints with requests
- Risk: Medium
- Mitigation: flask-limiter set to 30 requests/minute per IP

## Threat 4: Insecure Deserialization
- Description: Malicious JSON payload sent to API endpoints
- Risk: Medium
- Mitigation: Strict input validation, bleach sanitisation

## Threat 5: Excessive Data Exposure
- Description: AI response leaks sensitive internal data
- Risk: Medium
- Mitigation: PII audit on all prompts, no personal data sent to Groq
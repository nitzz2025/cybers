# Password Attack Methods Research Notes

## Brute Force Attacks

### Definition
Systematic method of trying every possible combination of characters until the correct password is found.

### How It Works
1. Attacker uses automated tools to generate password combinations
2. Each combination is tested against the target
3. Process continues until successful authentication or exhaustion
4. Modern tools can test millions of combinations per second

### Time Complexity Examples
- 8 characters (letters only): 45 minutes
- 8 characters (all types): 2 days
- 12 characters (all types): 34,000 years
- 16 characters (all types): 100+ trillion years

### Defense Methods
- Longer passwords (exponential increase in attack time)
- Account lockouts after failed attempts
- Rate limiting on login attempts
- Strong hashing algorithms (bcrypt, Argon2)

## Dictionary Attacks

### Definition
Using precompiled lists of common passwords, dictionary words, and known password patterns.

### Common Dictionaries Include
- Most common passwords (123456, password, qwerty)
- Dictionary words in multiple languages
- Names, places, dates
- Keyboard patterns (asdf, 1234)
- Previous breach data

### Sophisticated Variations
- **Hybrid attacks**: Dictionary words + numbers/symbols
- **Rule-based attacks**: Apply common transformations
- **Mask attacks**: Target specific patterns

### Statistics
- 80% of data breaches involve weak or stolen passwords
- Top 25 passwords account for 10% of all passwords
- Average user has 70-80 online accounts

### Defense Methods
- Avoid dictionary words entirely
- Use random passphrases
- Implement password policies blocking common passwords
- Regular password audits against known lists

## Rainbow Table Attacks

### Definition
Using precomputed tables of hash values for common passwords to reverse hash functions quickly.

### Process
1. Attacker obtains hashed passwords from data breach
2. Compares hashes against precomputed rainbow tables
3. Finds matches to reveal original passwords
4. Much faster than real-time hash computation

### Defense Methods
- Salt passwords before hashing
- Use slow hash functions (bcrypt, scrypt, Argon2)
- Regular password resets after breaches
- Monitor for credential stuffing attempts

## Social Engineering Attacks

### Common Methods
- **Phishing**: Fake login pages to capture credentials
- **Shoulder surfing**: Observing password entry
- **Pretexting**: Impersonating authority figures
- **Baiting**: Offering something to get password access

### Personal Information Exploitation
- Birthdays, anniversaries, pet names
- Family member names
- Sports teams, hobbies
- Work-related information

### Defense Methods
- Password education and awareness training
- Multi-factor authentication
- Regular security awareness updates
- Incident reporting procedures

## Modern Attack Trends

### Credential Stuffing
- Using breached credentials across multiple sites
- Automated tools test credentials on thousands of sites
- Successful due to password reuse

### Password Spraying
- Testing common passwords against many accounts
- Avoids account lockouts by staying under threshold
- Targets organizations with predictable password policies

### AI-Enhanced Attacks
- Machine learning to improve password guessing
- Analysis of personal data to create targeted wordlists
- Automated social engineering campaigns

## Key Research Sources
- NIST Special Publication 800-63B
- OWASP Authentication Guidelines
- Have I Been Pwned breach database
- Verizon Data Breach Investigations Report
- Academic papers on password security

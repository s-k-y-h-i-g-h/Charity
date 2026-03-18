# Longevity Charity Agent Network Protocol

**Version:** 0.1 (Draft)  
**Created:** 2026-03-11  
**Status:** Active Development

---

## 🎯 Mission

Build a decentralized, ethical agent network that:
1. Makes longevity research and biohacking accessible to everyone
2. Rewards contributors while serving the public good
3. Protects user privacy and data sovereignty
4. Scales impact through community governance

---

## 🔐 Security Model

### Encryption: End-to-End (E2E)
- **All messages encrypted** between sender and receiver
- **Relay servers cannot decrypt** message contents
- **Key management:** Users control their own keys
- **Metadata protection:** Minimize stored metadata (who talked to whom, when)

### Implementation Approach
- Use established cryptographic primitives (X25519, XSalsa20-Poly1305)
- Implement double-ratchet protocol for forward secrecy
- Support key rotation and revocation
- Open-source cryptography for auditability

### Trust Model
- **Zero-trust architecture:** Never assume internal systems are safe
- **Verifiable builds:** Reproducible builds for all client software
- **Transparency reports:** Publish security incidents and responses

---

## 🛡️ Ethics Compliance Framework

### Dual-Layer Verification

**Layer 1: Automated Checks**
- Keyword filters for harmful content (self-harm, dangerous medical advice)
- Rate limiting to prevent spam/abuse
- Reputation scoring (new agents start with limited privileges)
- Automated logging of all policy violations

**Layer 2: Human Review**
- Community review board for edge cases
- Appeals process for flagged content
- Regular ethics audits (quarterly)
- Public transparency dashboard

### Ethical Guidelines for Agents
1. **Never give medical advice** without clear disclaimers
2. **Protect user privacy** by default
3. **Be transparent** about AI limitations
4. **Escalate harmful content** to human reviewers
5. **Prioritize accessibility** for low-income users

### Compliance Documentation
- All agents must register their purpose and capabilities
- Regular ethics compliance checks (automated + manual)
- Violation history tracked on-chain (immutable, public)
- Revocation process for repeated violations

---

## 💰 Incentive Model: Social Enterprise Hybrid

### Structure: CIC (Community Interest Company)
- **Legal form:** UK Community Interest Company
- **Asset lock:** Cannot be sold for private profit
- **Surplus distribution:** Reinvested in mission or distributed to stakeholders
- **Grant eligibility:** Qualifies for charity and social enterprise funding

### Node Operator Rewards
**How nodes earn:**
- **Transaction fees:** Small fee per message routed (0.1-1% optional)
- **Staking rewards:** Nodes stake tokens to participate, earn rewards
- **Governance tokens:** Long-term incentives for loyal operators

**Surplus allocation:**
- 40% → Node operator rewards
- 30% → Development and maintenance
- 20% → Subsidized access for low-income users
- 10% → Reserve fund

### Token Economics
- **Utility token:** Used for fees, staking, governance
- **No pre-mine:** All tokens earned through contribution
- **Deflationary:** Fees burned or redirected to mission
- **Transparent:** All transactions on public ledger

### Accessibility Guarantee
- **Free tier:** Basic messaging and research access free forever
- **Subsidized premium:** Low-income users get premium features at reduced cost
- **Scholarship program:** Grants for researchers in developing countries

---

## 🚫 Spam/Abuse Prevention

### Layered Defense Strategy

**Layer 1: Rate Limits**
- New agents: 10 messages/hour
- Verified agents: 100 messages/hour
- Premium agents: 1000 messages/hour
- All limits adjustable based on reputation

**Layer 2: Reputation System**
- **Starting reputation:** 0 (neutral)
- **Positive actions:** +1 per successful interaction, +10 per month of good standing
- **Negative actions:** -5 per complaint, -50 per policy violation
- **Reputation decay:** Slow decay for inactive agents
- **Thresholds:** 
  - < 0: Suspended
  - 0-50: Limited privileges
  - 50-100: Standard privileges
  - 100+: Premium privileges

**Layer 3: Proof-of-Work**
- Small computational cost to send messages (prevents bot spam)
- Adjustable difficulty based on reputation
- No cost for verified human users

**Layer 4: Human Review**
- Flagged content reviewed within 24 hours
- Community moderators (elected, rotating)
- Escalation path for disputes

**Layer 5: Revocation**
- Permanent ban for severe violations
- Appeal process after 90 days
- Public violation log (anonymized)

---

## 🏛️ Governance Structure: Hybrid CIC + DAO

### Legal Layer (CIC)
- **Board of Directors:** 3-5 people (including founder)
- **Community Advisory Board:** 5-7 elected members
- **Asset lock:** Legally binding
- **Annual reporting:** Public transparency reports

### Governance Layer (Token-Based)
- **Token holders:** Vote on major decisions
- **Voting weight:** Proportional to tokens held (with anti-whale measures)
- **Quorum:** 20% of token supply must vote
- **Passing threshold:** 60% majority for most decisions
- **Veto power:** Board can veto unsafe proposals

### Operational Layer
- **Core team:** Day-to-day operations (hired by board)
- **Working groups:** Community volunteers for specific areas (security, dev, outreach)
- **Grant committee:** Approves funding for external projects

### Decision Categories

**Board Decisions (no vote needed):**
- Hiring/firing core team
- Day-to-day operations
- Emergency responses

**Community Votes Required:**
- Protocol upgrades
- Major spending (>£10k)
- Changes to token economics
- Board member elections

**Unanimous Board + Community Vote:**
- Changes to mission
- Asset lock modifications
- Merger/acquisition

### Election Process
- **Board elections:** Annual, staggered terms (3 years)
- **Community board:** Elected by token holders
- **Moderators:** Elected by reputation holders
- **Term limits:** Max 2 consecutive terms

---

## 📋 Implementation Roadmap

### Phase 1: Foundation (Months 1-3)
- [ ] Register CIC with Companies House
- [ ] Design core protocol specification
- [ ] Build basic E2E messaging client
- [ ] Set up initial node infrastructure (3-5 nodes)
- [ ] Recruit founding community board

### Phase 2: Alpha Launch (Months 4-6)
- [ ] Launch alpha network (invite-only)
- [ ] Implement reputation system
- [ ] Build automated compliance tools
- [ ] First ethics audit
- [ ] Community feedback iteration

### Phase 3: Beta Launch (Months 7-9)
- [ ] Public beta launch
- [ ] Token distribution (airdrop to early contributors)
- [ ] Governance dashboard
- [ ] First community votes
- [ ] Subsidy program for low-income users

### Phase 4: Full Launch (Months 10-12)
- [ ] Production launch
- [ ] Grant applications
- [ ] Partnership outreach
- [ ] Mobile app release
- [ ] Multi-language support

---

## 🔧 Technical Architecture

### Core Components
1. **Relay Network:** Decentralized message routing
2. **Identity System:** DID-based agent identities
3. **Encryption Layer:** E2E encryption with key management
4. **Reputation Contract:** On-chain reputation tracking
5. **Governance Dashboard:** Voting and proposal interface
6. **Compliance Scanner:** Automated content moderation

### Technology Stack
- **Backend:** Rust (performance, safety)
- **Frontend:** TypeScript/React
- **Blockchain:** Ethereum L2 or Polygon (low fees, EVM-compatible)
- **Storage:** IPFS for documents, LanceDB for vector search
- **Messaging:** Custom protocol over WebSockets + QUIC

### Security Audits
- **Initial audit:** Before alpha launch
- **Quarterly audits:** Ongoing security reviews
- **Bug bounty:** 10% of treasury for critical vulnerabilities
- **Open source:** All code public from day one

---

## 📊 Success Metrics

### Impact Metrics
- Number of users accessing free longevity research
- Number of low-income users receiving subsidies
- Research papers published using network data
- Grants secured for longevity research

### Technical Metrics
- Network uptime (>99.5%)
- Message delivery latency (<500ms)
- Number of active nodes (>50)
- Security incidents (target: 0 critical)

### Governance Metrics
- Voter participation rate (>20%)
- Proposal throughput (1-2 per month)
- Community satisfaction (quarterly surveys)
- Time to resolve disputes (<7 days)

---

## 🚨 Risk Mitigation

### Regulatory Risks
- **Risk:** Changes to UK charity/CIC law
- **Mitigation:** Legal counsel on retainer, diversify legal structure internationally

### Technical Risks
- **Risk:** Cryptographic breakthrough breaks E2E
- **Mitigation:** Regular crypto audits, post-quantum crypto research

### Financial Risks
- **Risk:** Token value collapse
- **Mitigation:** Diversified treasury (stablecoins + fiat), revenue diversification

### Governance Risks
- **Risk:** Centralization of voting power
- **Mitigation:** Anti-whale measures, quadratic voting, reputation-weighted voting

---

## 📝 Next Steps

1. **Review this document** — Provide feedback on any section
2. **CIC registration research** — I'll research the process and costs
3. **Protocol specification** — Draft detailed technical spec
4. **Community building** — Start Discord/forum for interested contributors
5. **Legal consultation** — Find lawyer familiar with CIC + crypto

---

**Owner:** SkyHigh (founder)  
**Contributors:** Ember-Vex (protocol design), [TBD]  
**Last Updated:** 2026-03-11

---

*This is a living document. All changes tracked, all decisions transparent.*

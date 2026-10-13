# 🔐 Cybersecurity Journal — Web Application Security

> **Understand the application. Form a hypothesis. Test it carefully. Explain the evidence.**

This repository is my hands-on journey into web application security, Burp Suite, and eventually my first valid Vulnerability Disclosure Program (VDP) report. I use it to record not only *what* I learn, but *how I reason about it*.

I'm especially interested in learning how to learn: building mental models, connecting concepts, practising deliberately, reducing distractions, and developing the focus to understand a subject deeply instead of rushing through checklists.

**This is a working journal, not a claim of expertise.** Checkboxes show the progress I have recorded here; a topic is not complete just because I watched a video or copied a payload.

---

## 🧭 Quick Navigation

- [My mission](#-my-mission)
- [Where I am right now](#-where-i-am-right-now)
- [Roadmap and progress board](#-roadmap-and-progress-board)
- [My testing methodology](#-my-testing-methodology)
- [PortSwigger learning order](#-portswigger-learning-order)
- [My lab notes](#-my-lab-notes)
- [My daily focus routine](#-my-daily-focus-routine)
- [Journey to my first VDP report](#-journey-to-my-first-vdp-report)
- [Definition of done](#-definition-of-done)

---

## 🎯 My Mission

I want to become capable of approaching an unfamiliar web application, understanding how it works, recognising where trust and permissions matter, testing sensible security hypotheses, and explaining the evidence clearly.

My learning principles:

- **Understand before memorising.** Know why a vulnerability exists, not only which payload triggered it.
- **Map before testing.** Learn the application's features, roles, requests, parameters, and state before testing randomly.
- **Change one variable at a time.** Keep experiments understandable and results comparable.
- **Prove, don't assume.** Separate observed behaviour from guesses and demonstrated impact from speculation.
- **Explain it in my own words.** If I cannot explain a concept without copying notes, I need to revisit it.
- **Build evidence of skill.** Publish useful notes, reproducible lab reasoning, and small tools as I develop them.
- **Protect my focus.** Work on one main topic at a time and value consistency over marathon sessions.

## 📍 Where I Am Right Now

> **Current phase:** Phase 1 — Web application mapping and Burp Suite fundamentals  
> **Current learning source:** [PortSwigger Web Security Academy](https://portswigger.net/web-security/learning-paths)  
> **Immediate goal:** Understand one complete browser-to-server interaction and document it clearly.

### This session's focus

- [ ] Choose one Academy lab and read its objective before testing.
- [ ] Use Burp to capture the relevant HTTP request and response.
- [ ] Identify the method, path, parameters, cookies, status code, and meaningful response changes.
- [ ] Explain what the feature should do under normal conditions.
- [ ] Write one testable security hypothesis before trying variations.
- [ ] Record the result and one question I still have.

**Next action:** Complete the first unchecked task above. When I finish a session, update this section so the next session starts with a clear action—not with deciding what to study.

<details>
<summary><strong>Session hand-off note — update after each study session</strong></summary>

- **Date:** YYYY-MM-DD
- **Topic / lab:**
- **What I understand now:**
- **What I tested:**
- **Evidence / result:**
- **What still confuses me:**
- **Next small action:**

</details>

---

## 🗺️ Roadmap and Progress Board

Use the checkboxes as the source of truth. Mark a phase complete only when its exit test feels achievable without following a solution step by step. If I need to revisit a topic, that is normal—not failure.

| Phase | Focus | Status | Exit test |
|---|---|---|---|
| **0** | Safe testing, HTTP basics, and lab setup | ⬜ Not yet recorded | I can explain the request/response cycle and stay within authorised scope. |
| **1** | Application mapping and Burp workflow | 🟡 Current | I can map a feature, capture traffic, and explain the important parts of the request and response. |
| **2** | Authentication and access control | ⬜ Not started | I can reason about identity, sessions, roles, ownership, and server-side authorisation. |
| **3** | Business logic and application state | ⬜ Not started | I can describe the intended workflow, identify unsafe assumptions, and design controlled tests. |
| **4** | Injection and input-handling vulnerabilities | ⬜ Not started | I can explain how untrusted input reaches a sensitive interpreter, output context, or file operation. |
| **5** | API testing and server-side attack surfaces | ⬜ Not started | I can inventory endpoints and test the relevant trust and authorisation boundaries. |
| **6** | In-scope VDP research and report writing | ⬜ Not started | I can submit a reproducible, safe, policy-compliant report with clear demonstrated impact. |

**Status key:** 🟡 Current · ⬜ Not started · 🔵 In progress · ✅ Completed · 🔁 Revisit

### Phase 0 — Foundations and safe workflow

- [ ] Understand HTTP requests and responses: method, path, headers, body, status code, cookies.
- [ ] Understand the roles of browser, frontend, server, database, and external services.
- [ ] Configure Burp Suite and its browser; understand Proxy and HTTP history.
- [ ] Use Repeater to resend a request and compare controlled changes.
- [ ] Learn the difference between authentication and authorisation.
- [ ] Understand that real-world testing requires explicit authorisation and a clear scope.

### Phase 1 — Map the application and learn Burp

- [ ] Browse a lab normally before changing requests.
- [ ] Record pages, actions, endpoints, HTTP methods, parameters, and relevant cookies.
- [ ] Identify which actions read data and which actions change state.
- [ ] Record important baseline requests and responses.
- [ ] Build a simple feature / endpoint inventory.
- [ ] Write one lab note using the template below.
- [ ] Explain the request journey without reading the note.

### Phase 2 — Authentication and access control

- [ ] Learn how sessions and cookies represent an authenticated state.
- [ ] Compare unauthenticated and authenticated behaviour in a lab.
- [ ] Understand user roles, object ownership, and server-side permission checks.
- [ ] Study direct object reference / broken object-level authorisation patterns.
- [ ] Learn common authentication and password-reset design weaknesses.
- [ ] Practise with accounts and data provided by the lab; never access real users' private data.
- [ ] Write a note that separates the expected rule, observed behaviour, and proven impact.

### Phase 3 — Business logic and state

- [ ] Map a multi-step workflow before testing it.
- [ ] Write down the rules the application appears to enforce.
- [ ] Look for assumptions involving sequence, repetition, quantities, prices, or state transitions.
- [ ] Test one assumption at a time in a controlled lab.
- [ ] Explain why the issue is a logic failure rather than merely unusual behaviour.

### Phase 4 — Input handling and injection

- [ ] SQL injection: understand how input interacts with database queries.
- [ ] Cross-site scripting (XSS): understand browser execution and output context.
- [ ] Path traversal: understand how file paths are built and constrained.
- [ ] File upload vulnerabilities: understand validation, storage, processing, and access.
- [ ] CSRF: understand browser credentials and unintended state-changing requests.
- [ ] For each topic, learn the root cause, safe proof, impact limits, and mitigation—not just a payload.

### Phase 5 — APIs and server-side attack surfaces

- [ ] Inventory API endpoints, methods, parameters, and response formats.
- [ ] Understand object-level and function-level authorisation in APIs.
- [ ] Study server-side request forgery (SSRF) in Academy labs.
- [ ] Compare API behaviour for different roles and application states.
- [ ] Learn how to document API requests and responses without leaking secrets.

### Phase 6 — Prepare for the first VDP report

- [ ] Choose one public program and read the entire policy before testing.
- [ ] Confirm the exact in-scope asset and allowed testing methods.
- [ ] Record exclusions, rate limits, prohibited tests, and reporting instructions.
- [ ] Map the application before selecting a small number of hypotheses.
- [ ] Stop once sufficient safe evidence is obtained; avoid destructive tests and real-user data.
- [ ] Check whether the issue is reproducible, in scope, security-relevant, and not a known exclusion.
- [ ] Write a concise report with steps, sanitised evidence, expected versus actual behaviour, and impact.
- [ ] Keep the outcome as a learning record, whether accepted, duplicate, informative, or out of scope.

---

## 🧪 My Testing Methodology

I want to use the same investigation cycle for every lab and, later, every explicitly authorised target.

```text
UNDERSTAND
    ↓
MAP THE FEATURE AND REQUESTS
    ↓
FORM ONE SECURITY HYPOTHESIS
    ↓
ESTABLISH A BASELINE
    ↓
CHANGE ONE VARIABLE AND TEST
    ↓
COMPARE THE EVIDENCE
    ↓
VERIFY IMPACT SAFELY
    ↓
EXPLAIN ROOT CAUSE AND MITIGATION
    ↓
DOCUMENT + RECALL FROM MEMORY
```

### Questions I ask about every feature

| Lens | Questions |
|---|---|
| **Identity** | Who does the application believe is making this request? |
| **Authority** | What should this user be allowed to read or change? Where is that enforced? |
| **Input** | Which values can the user influence? How are they validated and used? |
| **State** | What changes after this action? Does the order or repetition of actions matter? |
| **Data flow** | Where does an input go after the server receives it? |
| **Trust boundary** | Which component assumes another component has checked something? |
| **Evidence** | What did I observe directly? What am I only assuming? |
| **Impact** | What security consequence can I actually demonstrate? |

### My hypothesis format

> **I suspect** `[feature / endpoint]` may violate `[security rule]` because `[specific observation]`. I will compare `[baseline]` with `[one controlled change]`. If the result is `[expected evidence]`, it supports the hypothesis; if not, I will revise or reject it.

---

## 📚 PortSwigger Learning Order

This order is a practical study plan, not a requirement to complete every Academy lab before moving forward. Use the official learning material and labs; write the reasoning in my own words.

| Order | Topic | Resource | My progress |
|---:|---|---|---|
| 1 | Getting started with web security | [Getting started](https://portswigger.net/web-security/getting-started) | ⬜ |
| 2 | Burp Suite workflow and mapping | [Testing workflow](https://portswigger.net/burp/documentation/desktop/testing-workflow) | 🟡 |
| 3 | Access control | [Access control](https://portswigger.net/web-security/access-control) | ⬜ |
| 4 | Authentication | [Authentication vulnerabilities](https://portswigger.net/web-security/learning-paths/authentication-vulnerabilities) | ⬜ |
| 5 | Business logic | [Business logic vulnerabilities](https://portswigger.net/web-security/logic-flaws) | ⬜ |
| 6 | SQL injection | [SQL injection](https://portswigger.net/web-security/learning-paths/sql-injection) | ⬜ |
| 7 | Cross-site scripting | [Cross-site scripting](https://portswigger.net/web-security/cross-site-scripting) | ⬜ |
| 8 | File upload | [File upload vulnerabilities](https://portswigger.net/web-security/learning-paths/file-upload-vulnerabilities) | ⬜ |
| 9 | Path traversal | [Path traversal](https://portswigger.net/web-security/file-path-traversal) | ⬜ |
| 10 | CSRF | [CSRF](https://portswigger.net/web-security/csrf) | ⬜ |
| 11 | API testing | [API testing](https://portswigger.net/web-security/learning-paths/api-testing) | ⬜ |
| 12 | SSRF | [SSRF attacks](https://portswigger.net/web-security/learning-paths/ssrf-attacks) | ⬜ |

**Progress rule:** Mark a topic complete only after I can explain its core mechanism, solve representative labs without blindly following a walkthrough, identify the root cause, and describe a meaningful mitigation.

---

## 📝 My Lab Notes

Keep lab notes in my own words. Record the reasoning and the lesson, not just the successful input.

### Lab journal index

Add one row when I create or update a meaningful lab note. Link to the relevant Markdown file or folder in this repository.

| Date | Topic / lab | Key concept | Result | Notes |
|---|---|---|---|---|
| YYYY-MM-DD | First lab to document | HTTP request / response | In progress | Add link here |

Suggested result labels: `Solved independently`, `Solved with hints`, `Revisit`, `Concept understood`, `Blocked`.

### Reusable lab note template

Copy this section into a new Markdown file for each substantial lab.

```markdown
# [Lab name] — [Vulnerability class]

## 1. Goal and normal behaviour
- What feature am I testing?
- What should happen normally?

## 2. Mental model
- Browser → request → server → data / service → response
- Where does my input go?
- Which component should enforce the security rule?

## 3. Attack surface
- Endpoint and method:
- User-controlled inputs:
- Relevant cookies / session:
- Roles or preconditions:

## 4. Hypothesis
- Expected security rule:
- Possible broken assumption:
- Evidence that would support or reject my idea:

## 5. Experiments
| Test | One change | Observation | Conclusion |
|---|---|---|---|

## 6. Root cause
- What precisely went wrong?
- Why did the control fail?

## 7. Impact and limitations
- What can be demonstrated?
- Under what conditions?
- What remains unproven?

## 8. Mitigation
- What should the application enforce?
- How would I verify the fix?

## 9. Recall test
- Can I explain the issue without notes?
- Can I recognise the same pattern in another context?
- What related concept should I study next?

## 10. Next action
- One specific task for the next session:
```

---

## 🧠 My Daily Focus Routine

The aim is to make focused work repeatable—not to create a perfect schedule that collapses after one difficult day.

### One practical study cycle

1. **35 minutes — Learn and investigate.** One topic, one lab, one main objective. Keep unrelated tabs and notifications closed.
2. **10 minutes — Write the reasoning.** Record the baseline, hypothesis, experiment, evidence, and lesson.
3. **5 minutes — Recall without notes.** Explain what happened and why. Write down what remains unclear.

If 35 minutes feels too difficult on a particular day, start with 10 focused minutes and one small task. Consistency matters more than forcing a long session.

### Session checklist

- [ ] I chose one concrete task before starting.
- [ ] I kept unrelated distractions out of the session.
- [ ] I tested or explained something instead of only consuming content.
- [ ] I recorded at least one useful observation.
- [ ] I wrote the next action so I can restart easily.

---

## 🎯 Journey to My First VDP Report

The goal is to build the skill to produce a good report, not to guarantee a finding by a deadline. A VDP may be disclosure-only; monetary rewards depend on the individual program's terms.

### Before testing a real program

- [ ] Read the policy and confirm the exact asset is in scope.
- [ ] Understand prohibited activity, rate limits, account rules, and safe-harbour language.
- [ ] Use only accounts and data I am authorised to use.
- [ ] Avoid destructive actions, denial of service, social engineering, persistence, and unnecessary access to sensitive data.
- [ ] Stop after obtaining enough safe evidence to establish the issue.

### Report-writing checklist

- [ ] **Clear title:** identifies the affected feature and security failure.
- [ ] **Summary:** explains the weakness in plain language.
- [ ] **Affected asset:** exact in-scope host and endpoint.
- [ ] **Preconditions:** required role, account, or state.
- [ ] **Reproduction steps:** minimal, numbered, and repeatable.
- [ ] **Expected vs actual:** states the rule and what occurred.
- [ ] **Evidence:** sanitised requests, responses, and screenshots where useful.
- [ ] **Impact:** states what was demonstrated and avoids unsupported claims.
- [ ] **Remediation idea:** identifies the control or design that should change.
- [ ] **Policy check:** follows the program's submission and disclosure rules.

### First-report tracker

| Field | Record |
|---|---|
| Program | Not selected yet |
| Policy reviewed | ⬜ |
| In-scope asset verified | ⬜ |
| Feature mapped | ⬜ |
| Hypothesis tested | ⬜ |
| Finding reproduced safely | ⬜ |
| Report drafted | ⬜ |
| Report submitted | ⬜ |
| Outcome / lesson | Update when known |

---

## ✅ Definition of Done

A lab is not truly learned just because the Academy marks it solved. I should be able to:

- Explain the normal application behaviour and the security rule involved.
- Describe the relevant request, response, state, and trust boundary.
- Reconstruct the test from my notes without copying a solution blindly.
- Explain the root cause and a realistic mitigation.
- State exactly what the evidence proves—and what it does not prove.
- Connect the concept to at least one related topic.

## 📌 Repository Structure

As the journal grows, keep it easy to navigate. Use folders and links that match the files actually present in the repository.

```text
.
├── README.md                         # Progress dashboard and current focus
├── PortSwigger-Academy-Methodology/  # Methodology notes and topic guides
├── labs/                             # Individual lab write-ups (add as needed)
├── notes/                            # Concepts, diagrams, and revision notes (add as needed)
└── scripts/                          # Small, reviewed learning helpers (add as needed)
```

The folders shown as “add as needed” are a suggested future structure; create them only when they are useful.

---

## 🔗 Useful Resources

- [PortSwigger Web Security Academy](https://portswigger.net/web-security/learning-paths) — free learning paths and interactive labs.
- [Burp Suite documentation](https://portswigger.net/burp/documentation) — learn the tools and workflows.
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/) — a structured reference for web application testing.
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) — a broad awareness overview of major web application risk categories.

---

## Final Reminder

**The mission is not to rush through labs. It is to become better at observing, reasoning, testing, and explaining.**

One well-understood concept, documented honestly and revisited later, is worth more than a long checklist I cannot explain.

*Progress is measured by understanding I can demonstrate—not by how impressive the README looks.*

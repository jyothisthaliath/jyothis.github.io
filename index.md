---
layout: default
title: Jyothis George Thaliath | Information Security Leader
---

# Jyothis George Thaliath
**Information Security & Cybersecurity Manager**  
*Bridging the Gap Between Enterprise Risk Governance and Hands-On Infrastructure Architecture*

[LinkedIn](https://linkedin.com/in/jyothisthaliath) | [Technical Showcase](#technical-project-portfolio) | [Career & Achievements](career.html) | [Secure Contact](contact.html)

---

## Executive Profile
I manage enterprise security infrastructure and regulatory compliance within the banking sector. Over the past 13+ years, my work has focused on operating network security systems, modernizing Security Operations Centre (SOC), and coordinating technical project governance across cross-functional teams.

Outside of my day job, I maintain a home lab environment with self-hosted services. I experiment with automation scripts, and test infrastructure configurations. This site serves as a place to document those DIY projects and maintain a journal of my professional journey.

---

## Areas of Focus

*   **Security Operations & Infrastructure:** Practical experience implementing advanced enterprise defensive solutions and overseeing continuous operational coverage.
*   **Cybersecurity Governance & Compliance:** Navigating banking regulatory assessments (RBI) and technical audits
*   **Project & Vendor Coordination:** Managing technology procurement pipelines, commercial negotiations, and Change Approval Board (CAB) workflows.
*   **Data Protection & Perimeter Security:** Extensive background in Endpoint Protection, Data Loss Prevention (DLP), Zero Trust frameworks, and securing enterprise DNS/domain spaces.
*   **DevSecOps & Infrastructure Automation:** Practical experience with infrastructure orchestration, containerization (Docker)
*   **AI Implementation & Tooling: Developing conversational chatbots using large language models and incorporating AI-assisted workflows into code development. 

---

## Technical Project Portfolio
This section automatically tracks my hands-on DIY projects, infrastructure labs, and technical blueprints as I publish them. 

<ul>
  {% for page in site.pages %}
    {% if page.category == 'project' %}
      <li>
        <strong><a href="{{ page.url | relative_url }}">{{ page.title }}</a></strong>
        {% if page.description %}<br><small>{{ page.description }}</small>{% endif %}
      </li>
    {% endif %}
  {% endfor %}
</ul>

*(To see my full professional timeline, certifications, and banking sector accomplishments, please visit the [Career & Achievements](career.html) page.)*

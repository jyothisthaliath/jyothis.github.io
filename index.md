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

## GitHub Projects 
List of public repositories and open-source configurations hosted on my GitHub profile.
---

<div id="repo-list">Loading repositories...</div>

<script>
  const username = "jyothisthaliath";
  const container = document.getElementById("repo-list");

  fetch(`https://api.github.com/users/${username}/repos?sort=updated`)
    .then(response => {
      if (!response.ok) throw new Error("Failed to fetch repositories.");
      return response.json();
    })
    .then(repos => {
      // Filter out your profile README or pages repo if you want to hide them
      const filteredRepos = repos.filter(repo => repo.name !== `${username}.github.io`);

      if (filteredRepos.length === 0) {
        container.innerHTML = "<p>No public repositories found.</p>";
        return;
      }

      let html = '<ul style="list-style-type: none; padding-left: 0;">';
      filteredRepos.forEach(repo => {
        html += `
          <li style="margin-bottom: 1.5rem; border-bottom: 1px solid #eee; padding-bottom: 1rem;">
            <strong style="font-size: 1.2rem;">
              <a href="${repo.html_url}" target="_blank" rel="noopener noreferrer">${repo.name}</a>
            </strong>
            <p style="margin: 0.25rem 0; color: #555;">${repo.description || 'No description provided.'}</p>
            <small style="color: #888;">
              ${repo.language ? `<span>● ${repo.language}</span> &nbsp;&nbsp;` : ''}
              <span>Updated: ${new Date(repo.updated_at).toLocaleDateString()}</span>
            </small>
          </li>
        `;
      });
      html += '</ul>';
      container.innerHTML = html;
    })
    .catch(error => {
      container.innerHTML = `<p style="color: red;">Error loading repositories: ${error.message}</p>`;
    });
</script>

---


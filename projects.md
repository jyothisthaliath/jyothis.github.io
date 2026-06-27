---
layout: default
title: Technical Showcase
---

## Technical Project Portfolio

Things I am working on currently:

<ul class="project-card-list">
  {% for page in site.pages %}
    {% if page.category == 'project' %}
      <li class="project-card">
        <strong class="project-card-title">
          <a href="{{ page.url | relative_url }}">{{ page.title }}</a>
        </strong>
        {% if page.description %}
          <p class="project-card-desc">{{ page.description }}</p>
        {% endif %}
      </li>
    {% endif %}
  {% endfor %}
</ul>

## GitHub Repositories

Public repositories and open-source configurations from my GitHub profile:

<div id="repo-list"><p style="color: var(--text-muted); font-size: 0.875rem;">Loading repositories…</p></div>

<script>
  const username = "jyothisthaliath";
  const container = document.getElementById("repo-list");

  fetch(`https://api.github.com/users/${username}/repos?sort=updated&per_page=30`)
    .then(r => { if (!r.ok) throw new Error("Failed to fetch."); return r.json(); })
    .then(repos => {
      const filtered = repos.filter(r => r.name !== `${username}.github.io`);
      if (!filtered.length) { container.innerHTML = "<p>No public repositories found.</p>"; return; }

      let html = '<ul class="project-card-list">';
      filtered.forEach(repo => {
        const topics = repo.topics && repo.topics.length
          ? `<div class="project-card-topics">` +
            repo.topics.map(t => `<span class="project-card-tag">${t}</span>`).join('') +
            `</div>`
          : '';
        html += `
          <li class="project-card">
            <strong class="project-card-title"><a href="${repo.html_url}" target="_blank" rel="noopener noreferrer">${repo.name}</a></strong>
            <p class="project-card-desc">${repo.description || 'No description provided.'}</p>
            ${topics}
            <small class="project-card-meta">${repo.language ? `<span>● ${repo.language}</span> &nbsp;` : ''}<span>Updated: ${new Date(repo.updated_at).toLocaleDateString()}</span></small>
          </li>`;
      });
      html += '</ul>';
      container.innerHTML = html;
    })
    .catch(err => { container.innerHTML = `<p style="color:#cf222e; font-size:1rem;">Error loading repositories: ${err.message}</p>`; });
</script>

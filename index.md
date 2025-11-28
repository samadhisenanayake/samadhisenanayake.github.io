---
layout: default
title: "Samadhi Senanayake"
---

<a id="top"></a>

<section class="hero">
  <div class="container hero-content">
    <div class="hero-text">
      <h1 class="hero-name">Samadhi Senanayake</h1>
      <p class="hero-tagline">
        <strong>Microbiologist</strong> and <strong>Research Specialist</strong> with expertise in <strong>lamprey adaptive immunity</strong>,
        <strong>variable lymphocyte receptors</strong>, and <strong>infectious disease diagnostics</strong>.
      </p>
    </div>
    <div class="hero-image">
      <!-- Replace assets/img/profile.jpg with your own photo -->
      <img src="{{ '/assets/img/profile.jpg' | relative_url }}" alt="Profile photo of Samadhi Senanayake">
    </div>
  </div>

  <!-- Social Links and CV Download -->
  <div class="container">
    <ul class="hero-social-links">
      {% for item in site.data.social %}
        <li class="social-link-item">
          <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">
            <i class="{{ item.icon }}" aria-hidden="true"></i>
            <span class="social-name">{{ item.name }}</span>
          </a>
        </li>
      {% endfor %}
      <li class="social-link-item">
        <a href="{{ '/assets/CV_Samadhi_Senanayake.pdf' | relative_url }}" target="_blank" rel="noopener noreferrer" class="resume-download">
          <i class="fa fa-file-pdf-o" aria-hidden="true"></i>
          <span class="social-name">CV (PDF)</span>
        </a>
      </li>
    </ul>
  </div>
</section>

<section id="about" class="section section-alt">
  <div class="container">
    <h2>About</h2>
    <p>
      I am a <strong>Microbiologist</strong> at <strong>Voyant Beauty</strong> in Gainesville, Georgia, where I perform endotoxin screening,
      bacterial identification, sterility testing, and quality control analysis under GDP/GMP/USP guidelines. My work ensures product safety
      and regulatory compliance through rigorous microbiological testing and environmental monitoring.
    </p>
    <p>
      Previously, I served as a <strong>Research Specialist</strong> at <strong>Emory University School of Medicine</strong>, where I led
      research on the evolution of adaptive immune systems in lampreys. My work focused on developing monoclonal variable lymphocyte receptor
      (VLR) antibodies targeting <em>Plasmodium falciparum</em> and SARS-CoV-2, and identifying neutralizing antibodies with diagnostic and
      therapeutic potential. I performed extensive molecular and immunological techniques including PCR, ELISA, cloning, protein expression,
      hybridoma generation, flow cytometry, qPCR, and single-cell RNA sequencing.
    </p>
    <p>
      I hold a <strong>Bachelor's degree in Biology/Biological Sciences</strong> from <strong>Georgia State University</strong> (2020-2022)
      and a <strong>Bachelor's degree in Biology/Applied Bioscience</strong> from <strong>Kanazawa Institute of Technology</strong> in Japan
      (2015-2018). I am fluent in <strong>English</strong>, <strong>Japanese</strong>, and <strong>Sinhalese</strong>.
    </p>
    <p>
      My research has been published in peer-reviewed journals including <em>Scientific Reports</em>, and I have contributed to multiple
      studies advancing our understanding of lamprey immunity, antibody development, and infectious disease diagnostics.
    </p>
  </div>
</section>

<section id="research" class="section">
  <div class="container">
    <h2>Research Interests</h2>
    <p>
      My research focuses on the intersection of evolutionary immunology, antibody engineering, and infectious disease diagnostics:
    </p>
    <ul class="research-list">
      <li>
        <strong>Lamprey Adaptive Immunity:</strong> Investigating the unique variable lymphocyte receptor (VLR) system in lampreys,
        an ancient vertebrate lineage that provides insights into the evolution of adaptive immunity.
      </li>
      <li>
        <strong>VLR Antibody Development:</strong> Engineering and characterizing monoclonal VLR antibodies with diagnostic and therapeutic
        applications, including antibodies targeting malaria biomarkers and viral pathogens.
      </li>
      <li>
        <strong>Malaria Diagnostics:</strong> Developing thermostable VLR antibodies for detection of <em>Plasmodium falciparum</em>
        histidine-rich protein 2 (HRP-2), with applications in resource-limited settings.
      </li>
      <li>
        <strong>Evolutionary Immunology:</strong> Exploring proto-MHC signatures and the origins of adaptive immune recognition systems
        in jawless vertebrates.
      </li>
      <li>
        <strong>Protein Engineering & Structural Biology:</strong> Applying molecular biology techniques to characterize antibody-antigen
        interactions and develop novel diagnostic tools.
      </li>
      <li>
        <strong>Quality Control & Microbiology:</strong> Ensuring product safety and regulatory compliance through microbiological testing,
        method validation, and environmental monitoring in GMP-regulated environments.
      </li>
    </ul>

    <h3>Technical Expertise</h3>
    <div class="chips">
      <span class="chip">ELISA</span>
      <span class="chip">PCR & qPCR</span>
      <span class="chip">Molecular Cloning</span>
      <span class="chip">Protein Purification</span>
      <span class="chip">Western Blotting</span>
      <span class="chip">Hybridoma Production</span>
      <span class="chip">Flow Cytometry</span>
      <span class="chip">Single-Cell RNA-Seq</span>
      <span class="chip">HPLC & GC</span>
      <span class="chip">Microbiological Testing</span>
      <span class="chip">Endotoxin Testing</span>
      <span class="chip">Sterility Testing</span>
      <span class="chip">GMP/GDP Compliance</span>
      <span class="chip">Bioinformatics</span>
    </div>
  </div>
</section>

<section id="publications" class="section section-alt">
  <div class="container">
    <h2>Publications</h2>

    {% if site.data.publications and site.data.publications | size > 0 %}
      {% assign pubs_by_type = site.data.publications | group_by: "type" %}

      <!-- Journal Publications -->
      {% assign journal_pubs = site.data.publications | where: "type", "journal" | sort: "year" | reverse %}
      {% if journal_pubs.size > 0 %}
        <h3 class="publication-type-header">Journal Publications</h3>
        <ul class="publication-list">
          {% for pub in journal_pubs %}
            <li class="publication-item">
              <div class="publication-title">
                {% if pub.link %}
                  <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">{{ pub.title }}</a>
                {% else %}
                  {{ pub.title }}
                {% endif %}
              </div>
              <div class="publication-meta">
                {% if pub.authors %}<span class="pub-authors">{{ pub.authors }}</span>{% endif %}
                {% if pub.venue %}<span class="pub-venue"><em>{{ pub.venue }}</em></span>{% endif %}
                {% if pub.volume %}<span class="pub-volume">{{ pub.volume }}</span>{% endif %}
                {% if pub.year %}<span class="pub-year">({{ pub.year }})</span>{% endif %}
                {% if pub.doi %}<br><span class="pub-doi">DOI: <a href="https://doi.org/{{ pub.doi }}" target="_blank">{{ pub.doi }}</a></span>{% endif %}
              </div>
              {% if pub.summary %}
                <div class="publication-summary">{{ pub.summary }}</div>
              {% endif %}
            </li>
          {% endfor %}
        </ul>
      {% endif %}

      <!-- Preprints -->
      {% assign preprints = site.data.publications | where: "type", "preprint" | sort: "year" | reverse %}
      {% if preprints.size > 0 %}
        <h3 class="publication-type-header">Preprints</h3>
        <ul class="publication-list">
          {% for pub in preprints %}
            <li class="publication-item">
              <div class="publication-title">
                {% if pub.link %}
                  <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer">{{ pub.title }}</a>
                {% else %}
                  {{ pub.title }}
                {% endif %}
              </div>
              <div class="publication-meta">
                {% if pub.authors %}<span class="pub-authors">{{ pub.authors }}</span>{% endif %}
                {% if pub.venue %}<span class="pub-venue"><em>{{ pub.venue }}</em></span>{% endif %}
                {% if pub.year %}<span class="pub-year">({{ pub.year }})</span>{% endif %}
                {% if pub.doi %}<br><span class="pub-doi">DOI: <a href="https://doi.org/{{ pub.doi }}" target="_blank">{{ pub.doi }}</a></span>{% endif %}
              </div>
              {% if pub.summary %}
                <div class="publication-summary">{{ pub.summary }}</div>
              {% endif %}
            </li>
          {% endfor %}
        </ul>
      {% endif %}

    {% else %}
      <p>Publications coming soon.</p>
    {% endif %}

    <p style="margin-top: 2rem;">
      <a href="{{ '/publications.bib' | relative_url }}" class="bib-download">
        <i class="fa fa-download" aria-hidden="true"></i> Download BibTeX file
      </a>
    </p>
  </div>
</section>

<section id="cv" class="section">
  <div class="container">
    <h2>Curriculum Vitae</h2>

    <h3>Education</h3>
    <ul class="cv-list">
      <li>
        <strong>Bachelor's degree, Biology/Biological Sciences</strong><br>
        Georgia State University (May 2020 - December 2022)
      </li>
      <li>
        <strong>Bachelor's degree, Biology/Applied Bioscience</strong><br>
        Kanazawa Institute of Technology, Japan (January 2015 - July 2018)
      </li>
    </ul>

    <h3>Professional Experience</h3>
    <ul class="cv-list">
      <li>
        <strong>Microbiologist</strong> | Voyant Beauty, Gainesville, GA (November 2025 - Present)
      </li>
      <li>
        <strong>QC Analytical Technician</strong> | Voyant Beauty, Gainesville, GA (July 2025 - October 2025)
      </li>
      <li>
        <strong>Research Specialist</strong> | Emory University School of Medicine, Atlanta, GA (January 2025 - July 2025)
      </li>
      <li>
        <strong>Research Assistant</strong> | Emory University School of Medicine, Atlanta, GA (January 2023 - December 2024)
      </li>
      <li>
        <strong>Active Ingredient Technician</strong> | Boehringer Ingelheim, Athens, GA (July 2023 - July 2024)
      </li>
    </ul>

    <p style="margin-top: 2rem;">
      <a href="{{ '/assets/CV_Samadhi_Senanayake.pdf' | relative_url }}" class="cv-download-button" target="_blank" rel="noopener noreferrer">
        <i class="fa fa-file-pdf-o" aria-hidden="true"></i> Download Full CV (PDF)
      </a>
    </p>
  </div>
</section>

<section id="contact" class="section section-alt">
  <div class="container">
    <h2>Contact</h2>
    <p>
      I am currently based in <strong>Atlanta, Georgia</strong> and actively seeking opportunities in biotechnology R&D.
      Feel free to reach out via the links below:
    </p>
    <ul class="contact-links">
      {% for item in site.data.social %}
        <li class="social-link-item">
          <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">
            <i class="{{ item.icon }}" aria-hidden="true"></i>
            <span class="social-name">{{ item.name }}</span>
          </a>
        </li>
      {% endfor %}
    </ul>
  </div>
</section>

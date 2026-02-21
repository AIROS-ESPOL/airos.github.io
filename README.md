# 🤖 AIROS ESPOL - Official Website

This repository contains the source code of the official website of **AIROS (Artificial Intelligence and Robotics Society)** at ESPOL.

The site works as a living portfolio to showcase our robotics projects, scientific publications (papers), events, and to introduce our board members and general members.

🔗 **Website URL:** https://airos-espol.github.io/airos-web/

---

## 🛠 Technology

The site is built using **Jekyll**, a static site generator, and is hosted for free on **GitHub Pages**.

* **Framework:** Jekyll  
* **Styling:** Bootstrap (Base theme: Agency) + Custom CSS  
* **Icons:** FontAwesome 6 (via CDN)  
* **Fonts:** Google Fonts (Bebas Neue, Michroma, Montserrat, Rajdhani)

---

## 📂 Project Structure

Unlike a standard HTML page, this site is modular. Below is an explanation of where to edit each part:

### 1. Dynamic Information (`_data/` folder)
To simplify maintenance, repetitive information is stored in YAML files. **Edit these files to update content without touching HTML code.**

* `members.yml`: Database of the board and club members.
* `papers.yml`: List of scientific publications and accepted papers.
* `template.yml`: Global color and font configuration.

### 2. Projects and News (`_posts/` folder)
Each robot, workshop, or event is an individual file in this folder.
* **Filename format:** `YEAR-MONTH-DAY-title.md` (e.g., `2025-10-17-f1tenth.md`).
* **Requirement:** Each post must have a unique `modal-id` in its header so the popup window works correctly.

### 3. Page Sections (`_includes/` folder)
This folder contains the HTML blocks that make up the main page (`index.html`).
* `header.html`: The landing section with the large logo.
* `papers.html`: Scientific publications section.
* `services.html`: Departments section (Humanoids, Navigation, etc.).
* `join.html`: "Join Us" section with steps for applicants.
* `team.html`: Members grid layout.

### 4. Styles (`style.css` file)
Contains all the club's visual customizations (blue gradients, logo adjustments, futuristic fonts) that override the original theme.

---

## 🚀 Contributor Guide

### How to add a new member
1. Upload their photo (square JPG) to `img/team/`.
2. Open `_data/members.yml`.
3. Copy an existing member block and replace the data.

### How to publish a new project
1. Create a `.md` file in `_posts/`.
2. Use the standard template (see existing files).
3. Make sure to upload the images (normal and thumbnail) to `img/portfolio/`.

### Run locally
If you have Ruby and Jekyll installed:

```bash
bundle install
bundle exec jekyll serve
```

Access the site at http://localhost:4000.

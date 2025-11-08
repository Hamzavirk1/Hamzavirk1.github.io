# Hamza's Academic Website - Complete Guide

## 📋 Quick Reference

### Important Files to Edit:
- **About Page**: `_pages/about.md`
- **Publications**: `_bibliography/papers.bib`
- **CV Data**: `_data/cv.yml`
- **Site Configuration**: `_config.yml`
- **PDF Files**: `assets/pdf/`

---

## 🏠 1. Editing the About Section

**File**: `_pages/about.md`

### Basic Information
Edit the front matter (between the `---` lines):

```yaml
---
layout: about
title: about
permalink: /
subtitle: >
  Undergraduate Student<br>
  Department of Mathematics<br>
  <a href='https://www.hofstra.edu/'>Hofstra University</a>

profile:
  align: right
  image: prof_pic.png  # Replace with your photo in assets/img/
  image_circular: false
  more_info: >
    <p>Office: Your Office Number</p>
    <p>Hofstra University</p>
    <p>Hempstead, NY</p>
    <p><a href="/assets/pdf/hamza_virk_cv.pdf" class="btn btn-primary btn-sm" target="_blank"><i class="fas fa-download"></i> Download CV</a></p>
---
```

### Content Sections
Edit the main content below the `---`:

```markdown
## Welcome
Write your personal introduction here...

## Research Interests
- **Mathematical Finance**: Your specific interests
- **Stochastic Processes**: Areas you're studying
- **Computational Mathematics**: Methods you use

## Academic Philosophy
Describe your approach to learning and research...

## Current Work
Detail your ongoing projects and studies...
```

---

## 📚 2. Adding Publications

**File**: `_bibliography/papers.bib`

### Adding a New Paper
```bibtex
@article{unique_key_2025,
  abbr={VENUE},
  bibtex_show={true},
  title={Your Paper Title},
  author={Virk, Hamza and Coauthor, Name},
  journal={Journal Name},
  year={2025},
  month={January},
  pages={1--20},
  publisher={Publisher Name},
  selected={true},  # Shows on homepage if true
  url={https://link-to-paper.com},
  doi={10.1234/example},
  html={https://alternative-link.com},
  pdf={your_paper.pdf},  # Place PDF in assets/pdf/
  abstract={Your paper abstract goes here...},
  keywords={Keyword1, Keyword2, Keyword3}
}
```

### Important Fields:
- `selected={true}`: Shows on homepage
- `pdf={filename.pdf}`: Links to PDF (place in `assets/pdf/`)
- `url` or `html`: External links
- `abstract`: Paper summary
- `abbr`: Short venue name (appears as badge)

---

## 📄 3. Editing the CV Section

**File**: `_data/cv.yml`

### Adding Education
```yaml
- title: Education
  type: time_table
  contents:
    - title: Bachelor of Science in Mathematics
      institution: Hofstra University, Hempstead, NY
      year: 2022-2026
      description:
        - Concentration in Applied Mathematics
        - GPA: 3.8/4.0
        - Relevant Coursework: List your courses
```

### Adding Experience
```yaml
- title: Experience
  type: time_table
  contents:
    - title: Research Assistant
      institution: Department of Mathematics, Hofstra University
      year: 2024-Present
      description:
        - Working on mathematical finance projects
        - Developing computational models
```

### Adding Skills
```yaml
- title: Skills
  type: list
  contents:
    - <u>Programming:</u> Python, R, MATLAB, C++
    - <u>Software:</u> LaTeX, Git, Jupyter, Bloomberg Terminal
    - <u>Mathematics:</u> Stochastic Calculus, Real Analysis, Statistics
```

### Adding Awards
```yaml
- title: Awards
  type: time_table
  contents:
    - title: Dean's List
      year: 2023-2024
      description: Academic excellence recognition
```

---

## 🎓 4. Adding an Academics Section

### Option 1: Add to CV (Recommended)
Add to `_data/cv.yml`:

```yaml
- title: Coursework
  type: time_table
  contents:
    - title: Mathematics Courses
      year: 2022-2026
      description:
        - <strong>Core Mathematics:</strong> Calculus I-III, Linear Algebra, Differential Equations
        - <strong>Advanced Mathematics:</strong> Real Analysis, Abstract Algebra, Topology
        - <strong>Applied Mathematics:</strong> Numerical Analysis, Mathematical Modeling
        - <strong>Statistics:</strong> Probability Theory, Mathematical Statistics, Stochastic Processes
        - <strong>Finance:</strong> Mathematical Finance, Derivatives Pricing, Risk Management
    - title: Computer Science Courses
      year: 2022-2026
      description:
        - Programming Fundamentals (Python, C++)
        - Data Structures and Algorithms
        - Database Systems
        - Machine Learning
```

### Option 2: Create Separate Academics Page
Create `_pages/academics.md`:

```markdown
---
layout: page
title: academics
permalink: /academics/
description: My academic coursework and achievements
nav: true
nav_order: 3
---

## Mathematics Coursework

### Core Mathematics
- **Calculus I, II, III** - Differential and integral calculus
- **Linear Algebra** - Vector spaces, matrices, eigenvalues
- **Differential Equations** - Ordinary and partial differential equations

### Advanced Mathematics
- **Real Analysis** - Limits, continuity, differentiation, integration
- **Abstract Algebra** - Groups, rings, fields
- **Topology** - Point-set topology, metric spaces

### Applied Mathematics
- **Numerical Analysis** - Computational methods for mathematical problems
- **Mathematical Modeling** - Real-world problem solving
- **Optimization** - Linear and nonlinear programming

### Statistics and Probability
- **Probability Theory** - Measure theory, random variables
- **Mathematical Statistics** - Estimation, hypothesis testing
- **Stochastic Processes** - Markov chains, martingales

### Mathematical Finance
- **Financial Mathematics** - Time value of money, derivatives
- **Risk Management** - Portfolio theory, VaR models
- **Computational Finance** - Monte Carlo methods, numerical pricing

## Computer Science Coursework
- **Programming Fundamentals** - Python, C++, R
- **Data Structures and Algorithms** - Complexity analysis
- **Database Systems** - SQL, relational databases
- **Machine Learning** - Supervised and unsupervised learning

## Academic Achievements
- Dean's List: Fall 2023, Spring 2024
- Mathematics Department Honor Roll
- GPA: 3.8/4.0
```

Then add to navigation by editing `_config.yml`:
```yaml
nav_order: 3  # Add this to the academics page front matter
```

---

## 🌐 5. Publishing Your Website

### Option 1: GitHub Pages (Free & Easy)

1. **Enable GitHub Pages**:
   - Go to your repository: `https://github.com/sandroama/Hamza_VK`
   - Click "Settings" tab
   - Scroll to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

2. **Your website will be live at**: `https://sandroama.github.io/Hamza_VK/`

3. **Custom Domain (Optional)**:
   - Buy a domain (e.g., `hamzavirk.com`)
   - Add a `CNAME` file in repository root with your domain
   - Configure DNS settings with your domain provider

### Option 2: Netlify (Better Performance)

1. Go to [netlify.com](https://netlify.com) and sign up
2. Click "New site from Git"
3. Connect your GitHub repository
4. Build settings:
   - Build command: `bundle exec jekyll build`
   - Publish directory: `_site`
5. Deploy!

### Option 3: Vercel (Fast & Modern)

1. Go to [vercel.com](https://vercel.com) and sign up
2. Import your GitHub repository
3. Vercel auto-detects Jekyll
4. Deploy with one click

---

## 🔄 6. Making Changes and Updates

### Local Development Workflow:
1. **Start local server**: `bundle exec jekyll serve`
2. **View website**: Open `http://localhost:4000`
3. **Make changes** to files
4. **Test changes** locally
5. **Commit and push** to GitHub

### Git Workflow:
```bash
# Check what files changed
git status

# Add all changes
git add .

# Commit with descriptive message
git commit -m "Add new publication and update about section"

# Push to GitHub
git push origin main
```

### Automatic Updates:
- Once connected to hosting service, website updates automatically when you push to GitHub
- Changes typically appear within 1-5 minutes

---

## 📁 7. File Organization

### Key Directories:
- `_pages/`: Website pages (about, CV, publications, etc.)
- `_bibliography/`: Publication database
- `_data/`: Structured data (CV, social links, etc.)
- `assets/img/`: Images and photos
- `assets/pdf/`: PDF files (CV, papers, etc.)
- `_config.yml`: Main site configuration

### Adding Files:
- **Profile Photo**: Replace `assets/img/prof_pic.png`
- **CV PDF**: Add to `assets/pdf/hamza_virk_cv.pdf`
- **Paper PDFs**: Add to `assets/pdf/` and reference in bibliography

---

## 🎨 8. Customization Tips

### Colors and Themes:
- Edit `_sass/_themes.scss` for color schemes
- Choose from built-in themes in `_config.yml`

### Navigation:
- Add new pages to `_config.yml` navigation
- Set `nav: true` in page front matter

### Social Links:
- Edit `_data/socials.yml` for social media links
- Icons appear in footer and profile

### News/Announcements:
- Add files to `_news/` folder
- Shows on homepage if enabled

---

## 🚀 9. Quick Start Checklist

- [ ] Replace profile photo (`assets/img/prof_pic.png`)
- [ ] Update about section (`_pages/about.md`)
- [ ] Add your publications (`_bibliography/papers.bib`)
- [ ] Update CV information (`_data/cv.yml`)
- [ ] Add your actual CV PDF (`assets/pdf/hamza_virk_cv.pdf`)
- [ ] Test website locally (`bundle exec jekyll serve`)
- [ ] Push changes to GitHub (`git add . && git commit -m "Update website" && git push`)
- [ ] Enable GitHub Pages in repository settings
- [ ] Visit your live website!

---

## 📞 10. Troubleshooting

### Common Issues:
1. **Website not updating**: Check GitHub Actions tab for build errors
2. **Images not showing**: Ensure correct file paths and formats
3. **Bibliography not displaying**: Check BibTeX syntax
4. **Local server errors**: Run `bundle install` to update dependencies

### Getting Help:
- Check Jekyll documentation: [jekyllrb.com](https://jekyllrb.com)
- GitHub Pages guide: [pages.github.com](https://pages.github.com)
- Academic website examples: Browse other academic Jekyll sites

---

**Last Updated**: January 2025
**Website**: Your future live URL will be here!
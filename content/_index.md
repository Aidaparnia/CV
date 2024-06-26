---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Research Data Analyst
          company: Dalla Lana School of Public Health
          company_url: ''
          company_logo: university-of-toronto
          location: Toronto
          date_start: '2018-05-01'
          date_end: ''
          description: |2-
              Responsibilities include:

              - Developing research questions
              - Preparing and cleaning data
              - Constructing statistical models and visualizations
              - Drafting academic publication and presentations
        - title: CAnD 3 Fellow
          company: Consortium on Analytics for Data-Driven Decision-Making (CAnD3)
          company_url: ''
          company_logo: CAnD3
          location: Toronto
          date_start: '2023-09-01'
          date_end: ''
        - title: Research Assistant
          company: Queer & COVID Project
          company_url: ''
          company_logo: university-of-toronto
          location: Toronto
          date_start: '2022-09-01'
          date_end: '2023-09-01'
          description: |2-
              Responsibilities include:

              - Preparing and cleaning survey data
              - Developing survey weights
              - Creating visualizations
              - Drafting publications
        - title: Teaching Assistant
          company: University of Toronto - Sociology Department
          company_url: ''
          company_logo: university-of-toronto
          location: Toronto
          date_start: '2020-09-01'
          date_end: ''
          description: |2-
              Courses:
              - Intermediate Data Analysis (Graduate)     
              - Statistics for Sociologists (Graduate)     
              - Introduction to Quantitative Methods (Undergraduate)  
              - Sociology of Emotions (Undergraduate)  
              - Intermediate Quantitative Methods (Undergraduate)   
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Health
          tag: Health
        - name: Methods
          tag: Methods
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: collection
    id: featured
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card
  - block: collection
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        Feel free to contact me about my work.
      # Contact (add or remove contact options as necessary)
      email: a.parnia@utoronto.ca
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '43.6591996'
        longitude: '-79.3909595'  
      contact_links:
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: true
    design:
      columns: '2'
---

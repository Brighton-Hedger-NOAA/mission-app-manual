---
layout: default
title: Home
nav_order: 1
---

<style>
  /* Styles for the card layout */
  .card-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem; /* Space between cards */
    margin-top: 2rem;
    justify-content: center;
  }

  .info-card {
    flex: 1 1 300px; /* Flex-grow, flex-shrink, basis */
    max-width: 350px;
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    padding: 1.5rem;
    display: flex;
    flex-direction: column; /* Align content vertically */
    transition: transform 0.2s, box-shadow 0.2s;
  }

  .info-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 12px rgba(0,0,0,0.1);
  }

  .info-card h3 {
    margin-top: 0;
    color: #003366; /* Dark blue from your theme */
  }

  .info-card p {
    flex-grow: 1; /* Pushes the button to the bottom */
    color: #333;
  }

  /* Re-using your button style */
  .info-card .btn {
    text-decoration: none;
  }
</style>

# Welcome to the PIFSC Data Archiving Guide
This guide provides a step-by-step walkthrough of the entire data archiving process.

<div class="card-container">
  <div class="info-card">
    <h3>New to the Process?</h3>
    <p>Get oriented by reviewing the key terms, and systems before you begin the workflow.</p>
    <a href="{{ '/docs/The-Basics.html' | relative_url }}" class="btn btn-custom fs-5 mb-4 mb-md-0">
      Get Oriented
    </a>
  </div>

  <div class="info-card">
    <h3>Ready to Begin?</h3>
    <p>Jump directly into the Step 1 in the step-by-step of the full archival process.</p>
    <a href="{{ '/docs/Step-1-Planning.html' | relative_url }}" class="btn btn-custom fs-5 mb-4 mb-md-0">
      Get Started
    </a>
  </div>

  <div class="info-card">
    <h3>Attending the Workshop?</h3>
    <p>Find all the relevant guides and materials specifically for the Archive Refresher & Workshop.</p>
    <a href="{{ '/docs/Archive-Refresher&Workshop.html' | relative_url }}" class="btn btn-custom fs-5 mb-4 mb-md-0">
      Workshop Info
    </a>
  </div>
</div>



### <strong>Looking for something specific?</strong> Use the full navigation menu on the left or use the search bar at the top of the page!


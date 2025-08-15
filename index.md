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
  flex: 1 1 45%; 
  max-width: 450px; 
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


# Welcome to the NCRMP Mission App Manual
 This guide provides instructions and features for using the Mission App.

<div class="card-container">
  <div class="info-card">
    <h3>General Background</h3>
    <p>Understand what the Mission App is and how it fits into the NCRMP data workflow.</p>
    <center><a href="{{ '/docs/Background.html' | relative_url }}" class="btn btn-custom fs-5 mb-4 mb-md-0">
      Get Oriented
    </a></center>
  </div>

  <div class="info-card">
    <h3>Getting Started & Connected</h3>
    <p>Help with installation, account setup, and getting connected.</p>
    <center><a href="{{ '/docs/Connecting.html' | relative_url }}" class="btn btn-custom fs-5 mb-4 mb-md-0">
      Get Connected
    </a></center>
  </div>

  <div class="info-card">
    <h3>Data Entry</h3>
    <p>Walks through entering specific types of data.</p>
    <center><a href="{{ '/docs/import-workflow/index.html' | relative_url }}" class="btn btn-custom fs-5 mb-4 mb-md-0">
      Start the Data Entry Process
    </a></center>
  </div>

  <div class="info-card">
    <h3>Troubleshooting</h3>
    <p>Get solutions to common problems and learn what to do when things go wrong.</p>
    <center><a href="{{ '/docs/troubleshooting/index.html' | relative_url }}" class="btn btn-custom fs-5 mb-4 mb-md-0">
      Solve a Problem
    </a></center>
  </div>
</div>





### <strong>Looking for something specific?</strong> Use the full navigation menu on the left or use the search bar at the top of the page!


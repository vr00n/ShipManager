# Ship Management Platform

## Overview

This is a comprehensive web application designed to serve as a centralized dashboard for ship managers and technical superintendents. It provides a "single source of truth" to monitor vessel performance, manage maintenance, track procurement, and analyze fleet-wide KPIs. The application is built as a single, self-contained HTML file that runs entirely in the browser, using dynamically generated sample data to simulate a real-world fleet.

The platform is designed around a **Jobs to be Done (JTBD)** framework to ensure it directly addresses the critical daily tasks of a ship manager.

## Key Features

-   **Dynamic Dashboard:** An interactive dashboard that provides a high-level overview of a selected vessel, including its latest daily report, upcoming maintenance, recent purchase orders, and engine performance trends.
    
-   **Fleet-Wide Reporting:** Dedicated views for every major module (Vessel Reports, Maintenance, Surveys, etc.) that display data for the entire fleet.
    
-   **Vessel Filtering:** Each fleet view includes a dropdown to filter data and drill down to a specific vessel.
    
-   **Interactive Charts:** Key performance indicators are visualized with interactive charts, allowing users to analyze trends over various time periods.
    
-   **AI-Powered Analysis (Gemini API):** An integrated "Analyze Engine Trends" feature on the Engine Performance page that uses the Gemini API to provide expert-level insights and actionable recommendations based on recent engine data.
    
-   **Responsive Design:** A modern, two-column layout with a fixed sidebar for intuitive navigation, designed to work on various screen sizes.
    
-   **Zero Backend:** The entire application runs locally in the browser. It uses pre-generated sample data and does not require any database or server-side setup.
    

## Jobs to be Done Framework

This application was built to solve the following core jobs for a ship manager:

Job Story

Feature Implemented

**When I receive daily vessel reports,** I want to quickly review critical data (e.g., speed, fuel, incidents), so I can detect issues early.

The **Dashboard** and **Vessel Reports** tabs provide an at-a-glance view of the latest performance data for any selected vessel.

**When I log into the PMS,** I want to see overdue or upcoming maintenance tasks, so I can ensure regulatory compliance and avoid breakdowns.

The **Planned Maintenance** tab highlights overdue and upcoming jobs. The dashboard also shows a summary of near-term tasks.

**When a request for spares comes in,** I want to raise and track purchase orders, so I can ensure timely delivery and avoid delays.

The **Purchase Orders** tab provides a centralized view for tracking the status of all procurement requests across the fleet.

**When Class sends a report or schedule,** I want to plan surveys and document readiness, so I can keep certification up to date.

The **Class Surveys** tab lists all upcoming and scheduled surveys. The dashboard shows alerts for critical surveys (e.g., UWILD).

**When engine logs come in,** I want to analyze trends (e.g., fuel efficiency, wear), so I can take preventive measures.

The **Engine Performance** tab includes charts and data tables. The **AI Analysis** feature provides expert insights into trends and anomalies.

**When I open the app,** I want to see fleet-level KPIs (e.g., breakdowns, costs, performance), so I can assess operational effectiveness.

The main **Dashboard** presents key performance indicators, and each module provides a fleet-wide view with filtering capabilities.

## How to Run

This application is a single, self-contained `index.html` file with no build process required.

1.  **Local:**
    
    -   Download the `index.html` file.
        
    -   Open it directly in any modern web browser (like Chrome, Firefox, or Edge).
        
2.  **Web Hosting (GitHub Pages):**
    
    -   Create a new public repository on GitHub.
        
    -   Upload the `index.html` file to the repository.
        
    -   In the repository's settings, go to the "Pages" section.
        
    -   Select the `main` branch as the source and click "Save".
        
    -   The application will be live at `https://<your-username>.github.io/<your-repo-name>/`.
        

## Technology Stack

-   **Frontend:** React.js (loaded via CDN)
    
-   **Charting:** Chart.js (loaded via CDN)
    
-   **Styling:** Tailwind CSS (loaded via CDN)
    
-   **Date & Time:** date-fns (loaded via CDN)
    
-   **AI Integration:** Gemini API (via `fetch` calls)
    
-   **Transpilation:** Babel Standalone (for in-browser JSX transformation)

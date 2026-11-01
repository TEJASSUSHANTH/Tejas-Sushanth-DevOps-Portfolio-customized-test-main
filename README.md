# Tejas Sushanth H V — DevOps & Cloud Portfolio

A responsive, 3D-inspired personal portfolio built into the existing Java web application. The site is served as the root web app by Apache Tomcat and remains packaged as a WAR.

## Features
- Responsive layout with a 3D animated hero illustration
- Dark/light theme toggle
- Scroll reveal animations and subtle project-card tilt
- Animated terminal-style panel
- About, skills, projects, experience, certifications, GitHub, resume download, and contact sections
- Reduced-motion accessibility support

## Run with Docker
From this directory:

```bash
docker build -t tejas-portfolio .
docker run --rm --name tejas-portfolio -p 8080:8080 tejas-portfolio
```

Open http://localhost:8080/ . The existing servlet endpoint remains at http://localhost:8080/hello .

## Build a WAR locally
Requires JDK 17+ and Maven:

```bash
mvn clean package
```

The WAR is created at `target/my-java-app-1.0-SNAPSHOT.war`.

## Personalize before publishing
Search `src/main/webapp/index.jsp` for `your.email@example.com`, `https://github.com/`, and `your-username`. Replace these placeholders with your real contact/profile URLs. Update the starter resume at `src/main/webapp/assets/Tejas-Sushanth-HV-Resume.txt` with verified education, dates, experience, certificates, and project links. Do not claim certifications or work experience you do not have.

The listed projects are portfolio project ideas based on the existing Java WAR/Docker project and common beginner DevOps labs; update their descriptions to match what you have actually completed.

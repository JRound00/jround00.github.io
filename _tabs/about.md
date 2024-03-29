---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

# Welcome to My Cyber Security Portfolio

Hello! I'm a passionate Cyber Security Consultant and enthusiast, dedicated to exploring the depths of cyber security through practical engagement and continuous learning. This portfolio showcases my journey, including TryHackMe walkthroughs, participation in cyber security events, and various projects that highlight my skills and contributions to the field.

## TryHackMe Walkthroughs

I regularly engage with TryHackMe, an online platform for learning and teaching cyber security, all through hands-on experience. Here, you'll find detailed walkthroughs of challenges and rooms I've completed, providing insights into my problem-solving approach and technical expertise.

<ul>
{% assign recent_walkthroughs = site.walkthroughs | sort: 'date' | reverse | limit: 3 %}
{% for walkthrough in recent_walkthroughs %}
  <li>
    <a href="{{ site.baseurl }}{{ walkthrough.url }}">{{ walkthrough.title }}</a> - {{ walkthrough.date | date: "%B %d, %Y" }}
  </li>
{% endfor %}
</ul>

## Events

Participation in cyber security events is crucial for staying up-to-date with the latest threats and technologies. I've had the privilege of attending and sometimes speaking at various conferences and workshops.

- **[Event Name 1](#)**: My takeaways from this event and how it has influenced my approach to security.
- **[Event Name 2](#)**: A summary of my presentation or workshop, including any resources I shared.

## Projects

My projects range from developing security tools to contributing to open-source security software. These initiatives demonstrate my technical capabilities and commitment to improving cyber security practices.

- **[Project Name 1](#)**: Description of the project, the problem it solves, and the technologies used.
- **[Project Name 2](#)**: An overview of my contribution to this project and its impact on the community or end-users.

## Connect With Me

I'm always open to collaborating on projects or sharing knowledge with fellow security enthusiasts. Feel free to connect with me:

- **Email**: [your-email@example.com](mailto:your-email@example.com)
- **LinkedIn**: [Your LinkedIn Profile](https://www.linkedin.com)
- **GitHub**: [Your GitHub Profile](https://github.com)

Thank you for visiting my portfolio. Let's work together to make the digital world a safer place.
## Backend Developer with focus on Python microservices. Passionate about clean code, efficient algorithms, and scalable architecture.

```python
from dataclasses import dataclass, field
from typing import List, Dict, Optional

@dataclass
class Project:
    year: int
    name: str
    description: str
    role: str = "Solo Developer"
    technologies: List[str] = None
    repo_url: Optional[str] = None

@dataclass
class PythonBackendDeveloper:
    name: str = "Dmitry Vinogradov"
    age: int = 27
    title: str = "Backend Python Developer"
    contact_email: str = "vinodevelopment@gmail.com"
    github_username: str = "VinoStudio"
    primary_skills: Dict[str, List[str]] = field(default_factory=lambda: {
        "Languages": ["Python", "SQL", "JavaScript", "HTML", "CSS"],
        "Frameworks": ["FastAPI", "Litestar", "Django/DRF", "Flask", "React"],
        "Databases": ["PostgreSQL", "MySQL", "SQLite", "Redis", "MongoDB"],
        "DevOps/Cloud": ["Docker", "CI/CD (GitHub Actions)"],
        "Broker": ["RabbitMQ", "Kafka"],
        "Tools": ["Git", "Linux", "Postman", "PyCharm", "VSCode"],
    })
    learning_now: List[str] = field(default_factory=lambda: ["Algorithms and data structures", "System Design Patterns"])
    languages_speaking: List[str] = field(default_factory=lambda: ["Russian(native)", "English"])
    looking_for_work: bool = True
    contact_info: Dict[str, str] = field(default_factory=lambda: {
        "GitHub": "https://github.com/VinoStudio",
        "Email": "vinodevelopment@gmail.com",
        "Telegram": "@VinoGamer"
    })
    
    projects: Dict[int, List[Project]] = field(default_factory=lambda: {
        2023: [
            Project(
                year=2023,
                name: Homework for FullStack Developer course",
                description: "Food presentation Landing Page",
                role: "Solo Developer",
                technologies: ["HTML", "CSS", "JavaScript"],
                repo_url: "https://github.com/VinoStudio/food-landing-page"
            ),
            Project(
                year=2023,
                name: "Blog fullstack app on Django Framework",
                description: "DTF-like fullstack application using Django Framework and jinja templates",
                role: "Solo Developer",
                technologies: ["Django", "HTML", "CSS"],
                repo_url: "https://github.com/VinoStudio/Django_Blog"
            )   
        ],
        2024: [
            Project(
                year=2024,
                name: "Authentication Service with JWT, RBAC and FastAPI Framework",
                description: "RBAC based monilith authentication service using FastAPI Framework",
                role: "Solo Developer",
                technologies: ["FastAPI", "Celery", "Redis", "PostgreSQL", "SQLAlchemy"],
                repo_url: "https://github.com/VinoStudio/fastapi-auth-service"
            ),
            Project(
                year=2024,
                name: "React Food Delivery App",
                description: "React based food delivery app",
                role: "Solo Developer",
                technologies: ["React", "Vite", "HTML", "CSS"],
                repo_url: "https://github.com/VinoStudio/food_delivery_react"
            )
        ],
        2025: [
            Project(
                year=2025,
                name: "User services with FastAPI Framework",
                description: "Microservice that describles user profile, connect with Auth Service by Kafka",
                role: "Solo Developer",
                technologies: ["FastAPI", "PostgresQL", "SQLAlchemy", "Kafka"],
                repo_url: "https://github.com/VinoStudio/user_service"
            ),
            Project(
                year=2025,
                name: "Auth Microservice with Litestar Framework",
                description: "Microservice that implements user authentication, rbac, OAuth and connected with User Service by Kafka",
                role: "Solo Developer",
                technologies: ["Litestar", "PostgresQL", "SQLAlchemy", "Redis", "Celery", "Grafana", "Kafka"],
                repo_url: "https://github.com/VinoStudio/auth_service"
            )
        ]
    })
    
    def philosophy(self) -> str:
        return "My Philosophy: 'Readability counts. If the implementation is hard to explain, it's a bad idea.' (Zen of Python, adapted)"
    
    def calculate_experience(self) -> str:
        return f"{2025 - 2023} years of development experience"
        
    def __str__(self) -> str:
    return f"{self.name} | {self.title} | {self.primary_skills['Languages'][0]} Developer"



if __name__ == "__main__":
    me = PythonBackendDeveloper()
    print(me)
    print(me.philosophy())
    print(f"Contact me at: {me.contact_email}")

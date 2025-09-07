# ⚡ .NET 9 Web API | Dockerized

A **.NET 9 Web API** containerized with **Docker**, featuring a **multi-stage build** for smaller, production-ready images.  

---

## 🚀 Features
- 🌐 RESTful API built with **.NET 9**
- 📦 Multi-stage Docker build (optimized image size)
- ⚙️ Ready for deployment on Kubernetes or cloud providers
- Lightweight final Docker image
- Exposes port **8080**
- 🐳 Dockerized for portability and consistency
- 🔄 CI/CD friendly setup

---

## 🛠️ Tech Stack
- **Backend:** .NET 9 (ASP.NET Core Web API)
- **Containerization:** Docker
- **Language:** C#

---

## 📂 Project Structure

dotnet-api-dockerized/
│── Properties/ # Launch settings
│── Dockerfile # Multi-stage Docker build
│── Program.cs # Entry point
│── dotnetapi.csproj # Project file
│── appsettings.json # Configurations
│── appsettings.Development.json


---

## 🐳 Docker Setup

### 1️⃣ Build the Docker Image
```
docker build -t your-dockerhub-username/dotnet-api:latest .

```
### 2️⃣ Run the Container
```
docker run -d -p 8080:8080 your-dockerhub-username/dotnet-api:latest
```

Access API at 👉

http://localhost:8080

## 📸 Screenshot

Here’s the API running successfully in the browser:

(

## ☸️ Kubernetes Deployment (Optional)

If deploying to Kubernetes, create a deployment manifest like:
```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: dotnet-api-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: dotnet-api
  template:
    metadata:
      labels:
        app: dotnet-api
    spec:
      containers:
      - name: dotnet-api
        image: your-dockerhub-username/dotnet-api:latest
        ports:
        - containerPort: 8080
```

And expose it with a service.


## 🔮 Future Improvements

- Add Swagger for API documentation

- Integrate with PostgreSQL/MongoDB

- CI/CD pipeline (GitHub Actions / Jenkins)

- Deploy on Kubernetes with Helm

- Add monitoring (Prometheus + Grafana)

## 👩‍💻 Author

#### Maryam Abdulrauf
**DevOps Engineer | Cloud & Automation Enthusiast** 🚀

## ⭐ Contributions

Pull requests are welcome! For major changes, open an issue first to discuss your ideas.

## 📜 License

MIT License


---


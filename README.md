![banner](./assets/banner.png)
<h1 align="center">Ledgerly</h1>
<p align="center">
An open-source, self-hosted expense tracking platform powered by Next.js and Python, with AWS handling Lambda functions and S3 storage. Track your spending effortlessly and gain meaningful financial insights.
</p>

<p align="center">·
  <a href="#overview"><strong>Overview</strong></a> ·
  <a href="#tech-stack"><strong>Tech-Stack</strong></a> .
</p>

## overview
<img alt="AWS Architecture" src="./assets/arch.png">

- User feeds in an Image of the reciept, creating an object
- When an object is created in **s3** it triggers an event notification.
- Which then triggers a **Lambda** function to create an expense record.
- This expense record is created by feeding it to **Gemini Vision Model API**, which returns the reciept data.
- The expense record is then stored in a **RDS** running on postgreeSQL.
- The backend is run on an **EC2** instance , which registers an user ,create expense record ,uploads  reciept image to a S3.
- All of these services are run using **Docker** containers to ensure availability and performance.

### Tech Stack
![NextJs](https://img.shields.io/badge/Nextjs-black?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-blue?style=for-the-badge&logo=python&logoColor=white)
![Uvicorn](https://img.shields.io/badge/uvicorn-E6526F.svg?style=for-the-badge&logo=gunicorn&logoColor=white)
![EC2](https://img.shields.io/badge/ec2-orange?style=for-the-badge&logo=amazon-ec2&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![ECR](https://img.shields.io/badge/ecr-f06611.svg?style=for-the-badge&logo=square&logoColor=white)
![S3](https://img.shields.io/badge/S3-darkgreen?style=for-the-badge&logo=amazon-s3&logoColor=white)
![Lambda](https://img.shields.io/badge/Lambda-FF9900?style=for-the-badge&logo=aws-lambda&logoColor=white)
![Gemini](https://img.shields.io/badge/gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Traefik](https://img.shields.io/badge/Traefik-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)



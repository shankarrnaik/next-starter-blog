<img src="https://og-image.vercel.app/**NEXT.js%20Starter%20Blog**%3Cbr%20%2F%3EStarter%20blog%20with%20MDX%2C%20Tailwind%20CSS%2C%20and%20TypeScript..png?theme=dark&md=1&fontSize=100px&images=https%3A%2F%2Fassets.vercel.com%2Fimage%2Fupload%2Ffront%2Fassets%2Fdesign%2Fhyper-bw-logo.svg" />

# <p align="center">NEXT.js Starter Blog</p>

<p align="center">
  <b>NEXT.js starter blog with MDX, Tailwind CSS, TypeScript, and pre-configured Development Environment with Husky, Lint Staged and Commitizen.</b>
</p>

**Tech Stack:**

- 👾 NEXT.js for the core
- 🌀 Jotai for your app's state
- 🧰 TypeScript
- 📝 MDX for the Blog
- 💅 Tailwind CSS for styling
- 🌠 Framer Motion for animation
- 💎 Prism to highlight your code blocks

**Installation**

#### Bare Machine
- yum install -y git docker npm
- git clone https://github.com/devsecops-learning/next-starter-blog.git
- cd next-starter-blog/
- npm install
- npm run build
- npm start

#### Docker Container

- Start Docker Service Execute `systemctl enable --now docker`

- Create Dockerfile & add below content
```
# Specify the parent image from which we build
FROM node:latest

# Set the working directory
WORKDIR /app

# Copy files from your host to your current working directory
COPY . /app

# Build the application with cmake
RUN npm install && npm run build

#Expose Port
EXPOSE 3000

# Run the application
CMD ["npm", "start"]
```
- Execute `docker build -t next-starter-blog-docker:v1 .`
- Execute `docker run -d -p 3000:3000 --name next-starter-blog-docker-v1 next-starter-blog-docker:v1`
- Check `netstat -nltop`
- curl localhost:3000

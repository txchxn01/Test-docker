# ใช้ Node.js เป็น base image
FROM node:18-alpine

# ตั้งค่า working directory
WORKDIR /app

# คัดลอกไฟล์ package.json และ package-lock.json
COPY package.json package-lock.json ./

# ติดตั้ง dependencies
RUN npm install

# คัดลอกโค้ดทั้งหมดไปยัง container
COPY . .

# Build Next.js application
RUN npm run build

# กำหนด Port ที่จะ expose
EXPOSE 3000

# คำสั่งสำหรับรันแอป
CMD ["npm", "run", "start"]

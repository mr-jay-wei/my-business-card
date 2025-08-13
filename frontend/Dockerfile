# 1. 选择一个Node.js基础镜像
FROM node:[版本]-alpine AS build-stage 
# 2. 设置工作目录
WORKDIR /app
# 3. 复制依赖定义文件
COPY package*.json ./
# 4. 安装依赖 (利用缓存)
RUN npm install
# 5. 复制所有源代码
COPY . .
# 6. 执行构建命令
RUN npm run build

# 1. 选择一个Web服务器基础镜像
FROM nginx:stable-alpine
# 2. 从“构建阶段”搬运“物资包”到“展台”的根目录
COPY --from=build-stage /app/dist /usr/share/nginx/html 
# 3. 把我们的“工作指南”交给管理员
COPY nginx.conf /etc/nginx/conf.d/default.conf
# 4. Nginx镜像的默认CMD就是启动Nginx服务，我们无需重写
EXPOSE 80
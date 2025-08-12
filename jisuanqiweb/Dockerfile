FROM python:3.9-slim
WORKDIR /app

# 直接复制根目录的 requirements.txt
COPY requirements.txt .  
RUN pip install --no-cache-dir -r requirements.txt

# 复制根目录所有文件到容器的 /app
COPY . .  

EXPOSE 5000
CMD ["gunicorn", "main:app", "-b", "0.0.0.0:5000"]

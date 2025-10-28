# 名称

## 运行环境要求

- Python 3.11

## 部署步骤

1. 克隆项目到本地
   ```bash
   git clone <repository-url>
   cd <项目目录>
   ```

2. 创建并激活虚拟环境（推荐）
   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/Mac
   # 或
   venv\Scripts\activate      # Windows
   ```

3. 安装项目依赖
   ```bash
   pip install -r requirements.txt
   ```

4. 配置数据库
   在 `conf/application.yaml` 文件中配置数据库连接信息：
   ```yaml
   database:
     host: localhost       # 数据库主机地址
     port: 5432            # 数据库端口
     user: root            # 数据库用户名
     password: root        # 数据库密码
     name: decision_engine # 数据库名称
     charset: utf8mb4      # 字符集
   ```

5. 运行项目
   ```bash
   python main.py
   ```

6. 访问项目
   项目启动后，可以通过以下地址访问：
   - API文档: http://localhost:6789/docs
   - OpenAPI规范: http://localhost:6789/openapi.json
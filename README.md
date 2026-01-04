# FastAPI + Vue.js 全栈项目模板

这是一个通用的全栈Web应用开发模板，采用FastAPI作为后端框架，Vue.js作为前端框架，提供了完整的项目结构和基础功能。

## 项目结构

```
fastapi_framework/
├── backend/                    # 后端 FastAPI 服务
│   ├── api/                    # API 路由定义
│   │   └── index.py
│   ├── conf/                   # 配置文件
│   │   └── application.yaml    # 应用配置
│   ├── middleware/             # 中间件
│   │   └── http_log_middleware.py
│   ├── repository/             # 数据访问层
│   │   ├── base_repository.py
│   │   ├── data_struct.sql
│   │   └── models.py
│   ├── utils/                  # 工具类
│   │   ├── tests/
│   │   │   └── test.py
│   │   ├── constains.py
│   │   ├── database.py
│   │   ├── exception.py
│   │   ├── logger.py
│   │   ├── other.py
│   │   ├── response.py
│   │   └── system.py
│   ├── main.py                 # 应用入口
│   └── requirements.txt        # Python 依赖
└── frontend/                   # 前端 Vue.js 项目
    ├── public/
    │   └── index.html
    ├── src/
    │   ├── api/
    │   │   └── api.ts
    │   ├── components/
    │   │   └── HelloWorld.vue
    │   ├── router/
    │   │   └── index.ts
    │   ├── utils/
    │   │   ├── axios.ts
    │   │   └── public.ts
    │   ├── App.vue
    │   ├── main.ts
    │   └── shims-vue.d.ts
    ├── babel.config.js
    ├── openapitools.json
    ├── package-lock.json
    ├── package.json
    ├── tsconfig.json
    └── vue.config.js
```

## 技术栈

### 后端 (FastAPI)
- **FastAPI**: 高性能Web框架，支持异步处理
- **Python**: 3.x 版本
- **数据库**: PostgreSQL (默认配置)
- **缓存**: Redis
- **ORM**: SQLAlchemy
- **日志**: loguru
- **配置管理**: YAML格式配置文件

### 前端 (Vue.js)
- **Vue.js**: 3.x 版本
- **TypeScript**: 类型安全
- **Vue Router**: 路由管理
- **Axios**: HTTP客户端
- **Ant Design Vue**: UI组件库
- **Sass**: CSS预处理器

## 功能特性

### 后端功能
- RESTful API设计
- 中间件支持 (HTTP日志记录)
- 数据库连接池管理
- 统一响应格式
- 异常处理机制
- 配置文件管理 (YAML格式)
- 环境变量支持

### 前端功能
- Vue 3 + TypeScript
- 模块化组件设计
- API接口统一管理
- 路由系统
- HTTP请求拦截器

## 快速开始

### 环境要求
- Python 3.8+
- Node.js 14+
- PostgreSQL
- Redis

### 后端启动

1. 安装Python依赖:
```bash
cd backend
pip install -r requirements.txt
```

2. 配置数据库连接:
修改 [backend/conf/application.yaml](file:///C:/Users/DELL/PycharmProjects/fastapi_framework/backend/conf/application.yaml) 文件中的数据库配置

3. 启动后端服务:
```bash
cd backend
python main.py
```

服务将运行在 `http://localhost:6789`

### 前端启动

1. 安装Node.js依赖:
```bash
cd frontend
npm install
```

2. 启动开发服务器:
```bash
npm run serve
```

前端开发服务器将运行在 `http://localhost:8080`

## 配置说明

项目配置文件位于 [backend/conf/application.yaml](file:///C:/Users/DELL/PycharmProjects/fastapi_framework/backend/conf/application.yaml)，包含以下配置项:

- **server**: 服务器配置 (端口、主机、环境等)
- **database**: 数据库连接配置
- **redis**: Redis连接配置
- **mcp**: 自定义配置项

## API文档

启动后端服务后，可以通过以下URL访问API文档:
- Swagger UI: `http://localhost:6789/docs`
- ReDoc: `http://localhost:6789/redoc`

## 开发规范

1. 遵循RESTful API设计原则
2. 使用TypeScript进行类型检查
3. 遵循代码风格指南
4. 编写单元测试

## 扩展功能

- 数据库迁移支持
- 用户认证和授权
- 日志管理
- 缓存策略
- API版本控制

## 部署

### 后端部署
使用Uvicorn部署生产环境:
```bash
uvicorn main:app --host 0.0.0.0 --port 6789 --workers 4
```

### 前端部署
构建生产版本:
```bash
npm run build
```

## 许可证

此项目为通用模板，可自由使用和修改。


# docker 安装mongodb和redis

- mongo用户名和密码

```javascript
    const connection = () => {
      return mongoose.connect(APP_CONFIG.MONGO_DB.uri, {
        // todo config @damon
        authSource: "admin",// 必填
        auth: {
            username: 'admin',
            password: '123456'
        }
      })
    }
```

# 配置tsconfig.json
- 使引用路劲更方便

```json
    "outDir": "./dist",
    "baseUrl": "./src",
    "paths": {
      "@app": ["./"],
      "@app/*": ["./*"]
    }
```

# admin后台初始无用户名， 默认密码"root"


# mongo数据导入和导出，便于迁移数据
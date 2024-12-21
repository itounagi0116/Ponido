# **PonidoSys：系统架构语言规范**

---

## **Baso-1: PonidoSys 的基础**

### **1.1 PonidoSys 的目标**
PonidoSys 是一种专为技术架构和文档撰写而设计的人工语言，目标是提供简洁且准确的表达。

- **技术专注**：适用于架构设计、技术文档和代码注释的撰写。  
- **国际兼容**：设计直观，便于多国技术团队理解和使用。  
- **简洁与一致性**：促进文档的一致性与标准化。  

---

## **Baso-2: 音系与符号**

### **2.1 音系**
PonidoSys 基于 Ponido 的音系，并扩展了用于技术术语的辅音。

- **元音**：a, i, u, e, o  
- **辅音**：k, s, t, n, h, m, r, y, w, p, d, z, v  

音系规则：
- CV（辅音+元音）或单个元音。  
  示例：*api*，*neto*，*veri*  

### **2.2 符号**
PonidoSys 使用以下符号来增强技术描述的清晰性：
- **@**：表示模块或方法名称。  
- **#**：用于注释和补充信息。  
- **::**：表示属性或设置。  
- **->**：表示依赖关系或数据流。  
- **<>**：表示输入和输出参数。

---

## **Baso-3: 语法结构**

### **3.1 词序**
PonidoSys 采用适合技术写作的词序：
- **SVO（主语-动词-宾语）**：用于标准技术描述。  
  示例：*System-ga module-o call-u.*  
- **OSV（宾语-主语-动词）**：用于强调宾语。  
  示例：*Module-o system-ga call-u.*

### **3.2 特殊句型**
1. **模块操作**：
   - *@ModuleName-ga method-o exec-u.*  
     示例：*@AuthModule-ga login-o exec-u.*

2. **依赖关系**：
   - *Process-A-ni Process-B-ga depend.*  
     示例：*Frontend-ni Backend-ga depend.*

3. **条件分支**：
   - *IF 条件 THEN 动作.*  
     示例：*IF error THEN exec-retry.*

---

## **Baso-4: 技术词汇**

### **4.1 技术动词**
系统设计和软件开发中常用的动词：
- *call-u*（调用）  
- *exec-u*（执行）  
- *send-u*（发送）  
- *receive-u*（接收）  
- *store-u*（存储）  
- *log-u*（记录日志）  
- *parse-u*（解析）  
- *deploy-u*（部署）  

### **4.2 技术名词**
PonidoSys 的核心名词：
- *module*（模块）  
- *data*（数据）  
- *process*（流程）  
- *api*（API）  
- *config*（配置）  
- *queue*（队列）  
- *cache*（缓存）  

---

## **Baso-5: 配置与资源管理**

### **5.1 属性描述**
属性和设置值使用 `[元素]:[值]` 的格式。
- 示例：  
  - *module:type=api.*  
  - *config:timeout=30.*  

### **5.2 资源管理**
资源分配和状态使用 `[资源]=[值]` 的格式。
- 示例：  
  - *Resource: CPU=multi, RAM=du.*  

---

## **Baso-6: 网络模型与依赖关系**

### **6.1 依赖关系描述**
模块或服务间的依赖关系表示为：
- 格式：`[A]-depend->[B]`  
  示例：  
  - *@ModuleA-depend->@ModuleB.*  
  - *Frontend->Backend:fetch-data.*

### **6.2 网络通信**
网络通信表示为：
- 格式：`[来源]->[目标]:[操作]`  
  示例：  
  - *Frontend->Backend:API-call.*  
  - *ServiceA->ServiceB:async-fetch.*

---

## **Baso-7: 注释与文档**

### **7.1 注释**
PonidoSys 使用 `#` 来表示注释。
- 示例：*# 该模块负责身份验证。*

### **7.2 自动文档生成**
以下标签用于自动生成文档：
- **@param**：描述参数  
- **@return**：描述返回值  
- **@throws**：描述可能的异常  
- **@doc**：提供模块或功能摘要  
  示例：  
  ```plaintext
  @doc: module-name="AuthModule", description="Handles user authentication"
  ```

---

## **Baso-8: 学习步骤**

### **8.1 学习计划**
1. **第1周**：学习基本语法和技术动词。  
2. **第2周**：练习条件分支和依赖关系描述。  
3. **第3周**：学习并应用网络通信模型。  
4. **第4周**：掌握配置描述和自动文档生成。  

### **8.2 实践练习**
- **系统设计**：使用 PonidoSys 描述模块间依赖关系。  
- **代码审查**：利用自动文档生成功能。  
- **网络通信**：记录网络数据流。

---

## **Baso-9: 示例句**

### **9.1 基本流程**
```plaintext
System-ga module-o call-u.  
(系统调用模块。)
```

### **9.2 条件分支**
```plaintext
IF error THEN exec-retry.  
(如果发生错误，则重试执行。)
```

### **9.3 网络通信**
```plaintext
Frontend->Backend:send-data.  
(前端向后端发送数据。)
```

### **9.4 依赖关系**
```plaintext
@AuthModule-depend->@Database.  
(认证模块依赖于数据库。)
```

---

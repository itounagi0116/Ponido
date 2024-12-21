# **PonidoSys: System Architecture Language Specification**

---

## **Baso-1: Fundamentals of PonidoSys**

### **1.1 Purpose of PonidoSys**
PonidoSys is a specialized artificial language designed to allow engineers and developers to concisely and accurately describe system architectures and technical documentation.

- **Technical Focus**: Simplify the writing of architecture designs, documentation, and code comments.  
- **International Compatibility**: Designed to be intuitive for engineers across multiple countries.  
- **Simplicity and Consistency**: Promote uniformity and standardization across team documentation.  

---

## **Baso-2: Phonology and Symbols**

### **2.1 Phonology**
PonidoSys builds on Ponido’s phonology, with additional consonants to accommodate technical terms.

- **Vowels**: a, i, u, e, o  
- **Consonants**: k, s, t, n, h, m, r, y, w, p, d, z, v  

Phonological rules:
- CV (Consonant + Vowel) or standalone vowels.  
  Examples: *api*, *neto*, *veri*  

### **2.2 Symbols**
PonidoSys introduces specific symbols to enhance clarity in technical descriptions:
- **@**: Indicates module or method names.  
- **#**: Used for comments and additional notes.  
- **::**: Denotes attributes or settings.  
- **->**: Represents dependencies or data flows.  
- **<>**: Specifies input and output parameters.

---

## **Baso-3: Grammar**

### **3.1 Word Order**
PonidoSys adopts word orders suitable for technical writing:
- **SVO (Subject-Verb-Object)**: Used for standard technical descriptions.  
  Example: *System-ga module-o call-u.*  
- **OSV (Object-Subject-Verb)**: Used to emphasize the object.  
  Example: *Module-o system-ga call-u.*

### **3.2 Special Syntax**
1. **Module Operations**:
   - *@ModuleName-ga method-o exec-u.*  
     Example: *@AuthModule-ga login-o exec-u.*

2. **Dependency Relations**:
   - *Process-A-ni Process-B-ga depend.*  
     Example: *Frontend-ni Backend-ga depend.*

3. **Conditional Statements**:
   - *IF condition THEN action.*  
     Example: *IF error THEN exec-retry.*

---

## **Baso-4: Technical Vocabulary**

### **4.1 Technical Verbs**
Key verbs for system design and software development:
- *call-u* (to call)  
- *exec-u* (to execute)  
- *send-u* (to send)  
- *receive-u* (to receive)  
- *store-u* (to store)  
- *log-u* (to log)  
- *parse-u* (to parse)  
- *deploy-u* (to deploy)  

### **4.2 Technical Nouns**
Core nouns in PonidoSys:
- *module* (module)  
- *data* (data)  
- *process* (process)  
- *api* (API)  
- *config* (configuration)  
- *queue* (queue)  
- *cache* (cache)  

---

## **Baso-5: Configuration and Resource Management**

### **5.1 Attribute Notation**
Attributes and settings are written in the format `[element]:[value]`.
- Examples:  
  - *module:type=api.*  
  - *config:timeout=30.*  

### **5.2 Resource Management**
Resources are described in the format `[resource]=[value]`.
- Examples:  
  - *Resource: CPU=multi, RAM=du.*  

---

## **Baso-6: Network Models and Dependencies**

### **6.1 Dependency Notation**
Dependencies between modules or services are represented as:
- Format: `[A]-depend->[B]`  
  Examples:  
  - *@ModuleA-depend->@ModuleB.*  
  - *Frontend->Backend:fetch-data.*

### **6.2 Network Communication**
Network communication is written as:
- Format: `[from]->[to]:[action]`  
  Examples:  
  - *Frontend->Backend:API-call.*  
  - *ServiceA->ServiceB:async-fetch.*

---

## **Baso-7: Comments and Documentation**

### **7.1 Comments**
PonidoSys uses `#` for comments.
- Example: *# This module handles authentication.*

### **7.2 Automatic Documentation**
Tags prefixed with `@` are used for generating documentation:
- **@param**: Describes parameters  
- **@return**: Describes return values  
- **@throws**: Describes exceptions  
- **@doc**: Provides module or function summaries  
  Example:  
  ```plaintext
  @doc: module-name="AuthModule", description="Handles user authentication"
  ```

---

## **Baso-8: Learning Steps**

### **8.1 Learning Plan**
1. **Week 1**: Learn basic grammar and technical verbs.  
2. **Week 2**: Practice conditional statements and dependencies.  
3. **Week 3**: Learn and apply network communication models.  
4. **Week 4**: Master configuration and automatic documentation.  

### **8.2 Practical Exercises**
- **System Design**: Write dependency relations using PonidoSys.  
- **Code Review**: Use automatic documentation tags.  
- **Network Communication**: Describe network flows.

---

## **Baso-9: Example Sentences**

### **9.1 Basic Process**
```plaintext
System-ga module-o call-u.  
(The system calls the module.)
```

### **9.2 Conditional Statement**
```plaintext
IF error THEN exec-retry.  
(If an error occurs, retry execution.)
```

### **9.3 Network Communication**
```plaintext
Frontend->Backend:send-data.  
(The frontend sends data to the backend.)
```

### **9.4 Dependency**
```plaintext
@AuthModule-depend->@Database.  
(The authentication module depends on the database.)
```

---

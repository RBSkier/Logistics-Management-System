# 物流管理系统项目介绍

## 1. 项目结构介绍

整个项目通过Maven聚合工程来构建，采用SpringMVC + Spring + MyBatis + MySQL + jsp

项目的目录结构
```txt
logistics-parent:父工程,打包方式pom，管理jar包的版本
	|        项目中所有的工程都应该继承父工程
	|--logistics-common:通用的工具类 打包方式jar
	|--logistics-manager:服务工程。聚合工程 Pom工程
		|--logistics-manager-pojo：打包方式jar
		|--logistics-manager-dao：打包方式jar
		|--logistics-manager-service：打包方式jar
		|--logistics-manager-web：打包方式war
```

## 2. 表结构
![image](https://github.com/RBSkier/Logistics-Management-System/assets/102810310/1385b279-73c8-4ba8-92f1-1086388f603b)

## 3. 业务功能
### 3.1.角色管理
#### 3.1.1 角色查询
```java
package com.bobo.service;

import com.bobo.pojo.Role;

import java.util.List;

/**
 * 角色信息
 */
public interface IRoleService {

    /**
     * 根据条件查询用户信息
     * @param role
     * @return
     */
    List<Role> query(Role role) throws Exception;

    /**
     * 添加用户信息
     * @param role
     * @return
     */
    Integer addRole(Role role) throws Exception;

    /**
     * 更新用户信息
     * @param role
     * @return
     */
    Integer updateRole(Role role) throws Exception;


    /**
     * 根据编号删除用户信息
     * @param id
     * @return
     */
    Integer deleteRole(Integer id) throws Exception;
}

```


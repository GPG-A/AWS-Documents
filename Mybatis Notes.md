## Mybatis特点：
    采用动态配置文件管理SQL语句，并含有输入映射、输出映射机制以及数据库连接池配置的持久层框架。
## Mybatis构造：
### SQL映射配置文件：
1. 数据源配置文件：SqlMapConfig.xml
2. SQL映射配置文件：Mapper.xml,所有数据库的操作都会基于该映射文件和配置的SQL语句
   
### 会话工厂与会话
1. 会话工厂：即SqlSessionFactory类，SqlSessionFactory类会根据Resource资源信息加载对象，获取项目配置中的数据库连接池配置文件SqlMapConfig.xml信息，从而产生一种可以与数据库交互的会话实例类SqlSession。
2. SQL映射配置文件Mapper.xml的路径是配置在SqlMapConfig.xml配置文件中的，所以SqlSessionFactory类同时也加载了SQL语句的配置信息。通过其产生的SqlSession会话实例类，可以依照Mapper配置文件中的SQL配置，对数据库执行增删改查的操作。
        
### 执行器
### 底层封装对象
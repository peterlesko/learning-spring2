Repo used in "Using a remote database session"

In 1:25min I got this error:

$ ./start_postgres.sh
./start_postgres.sh: line 9: docker: command not found




After updating pom file and application properties in 5:15min

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v2.1.9.RELEASE)

2020-10-03 22:50:58.291  INFO 16776 --- [           main] c.f.l.l.LearningSpringApplication        : Starting LearningSpringApplication on DESKTOP-TRKLV9E with PID 16776 (started by Pet in C:\Users\Pet\Documents\Learning\LinkedInLearning\Spring\Ex_Files_Learning_Spring_Spring_Boot\Exercise Files\Chapter2\02_04\02_04_begin\learning-spring)
2020-10-03 22:50:58.295  INFO 16776 --- [           main] c.f.l.l.LearningSpringApplication        : No active profile set, falling back to default profiles: default
2020-10-03 22:50:59.346  INFO 16776 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data repositories in DEFAULT mode.
2020-10-03 22:50:59.438  INFO 16776 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 80ms. Found 1 repository interfaces.
2020-10-03 22:50:59.892  INFO 16776 --- [           main] trationDelegate$BeanPostProcessorChecker : Bean 'org.springframework.transaction.annotation.ProxyTransactionManagementConfiguration' of type [org.springframework.transaction.annotation.ProxyTransactionManagementConfiguration$$EnhancerBySpringCGLIB$$26674922] is not eligible for getting processed by all BeanPostProcessors (for example: not eligible for auto-proxying)
2020-10-03 22:51:00.429  INFO 16776 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8080 (http)
2020-10-03 22:51:00.464  INFO 16776 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2020-10-03 22:51:00.464  INFO 16776 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.26]
2020-10-03 22:51:00.612  INFO 16776 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2020-10-03 22:51:00.613  INFO 16776 --- [           main] o.s.web.context.ContextLoader            : Root WebApplicationContext: initialization completed in 2237 ms
2020-10-03 22:51:00.753  INFO 16776 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2020-10-03 22:51:01.945 ERROR 16776 --- [           main] com.zaxxer.hikari.pool.HikariPool        : HikariPool-1 - Exception during pool initialization.

org.postgresql.util.PSQLException: FATAL: password authentication failed for user "postgres"
	at org.postgresql.core.v3.ConnectionFactoryImpl.doAuthentication(ConnectionFactoryImpl.java:520) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.core.v3.ConnectionFactoryImpl.tryConnect(ConnectionFactoryImpl.java:141) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.core.v3.ConnectionFactoryImpl.openConnectionImpl(ConnectionFactoryImpl.java:192) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.core.ConnectionFactory.openConnection(ConnectionFactory.java:49) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.jdbc.PgConnection.<init>(PgConnection.java:195) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.Driver.makeConnection(Driver.java:458) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.Driver.connect(Driver.java:260) ~[postgresql-42.2.8.jar:42.2.8]
	at com.zaxxer.hikari.util.DriverDataSource.getConnection(DriverDataSource.java:136) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.PoolBase.newConnection(PoolBase.java:369) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.PoolBase.newPoolEntry(PoolBase.java:198) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.HikariPool.createPoolEntry(HikariPool.java:467) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.HikariPool.checkFailFast(HikariPool.java:541) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:115) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:112) ~[HikariCP-3.2.0.jar:na]
	at org.springframework.jdbc.datasource.DataSourceUtils.fetchConnection(DataSourceUtils.java:158) ~[spring-jdbc-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.jdbc.datasource.DataSourceUtils.doGetConnection(DataSourceUtils.java:116) ~[spring-jdbc-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.jdbc.datasource.DataSourceUtils.getConnection(DataSourceUtils.java:79) ~[spring-jdbc-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.jdbc.core.JdbcTemplate.execute(JdbcTemplate.java:324) ~[spring-jdbc-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.boot.jdbc.EmbeddedDatabaseConnection.isEmbedded(EmbeddedDatabaseConnection.java:120) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.autoconfigure.jdbc.DataSourceInitializer.isEmbedded(DataSourceInitializer.java:136) ~[spring-boot-autoconfigure-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.autoconfigure.jdbc.DataSourceInitializer.isEnabled(DataSourceInitializer.java:128) ~[spring-boot-autoconfigure-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.autoconfigure.jdbc.DataSourceInitializer.createSchema(DataSourceInitializer.java:95) ~[spring-boot-autoconfigure-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.autoconfigure.jdbc.DataSourceInitializerInvoker.afterPropertiesSet(DataSourceInitializerInvoker.java:62) ~[spring-boot-autoconfigure-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1837) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1774) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:593) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:515) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:320) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:222) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:318) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:224) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveNamedBean(DefaultListableBeanFactory.java:1123) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveBean(DefaultListableBeanFactory.java:413) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.getBean(DefaultListableBeanFactory.java:346) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.getBean(DefaultListableBeanFactory.java:339) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.boot.autoconfigure.jdbc.DataSourceInitializerPostProcessor.postProcessAfterInitialization(DataSourceInitializerPostProcessor.java:52) ~[spring-boot-autoconfigure-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.applyBeanPostProcessorsAfterInitialization(AbstractAutowireCapableBeanFactory.java:429) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1782) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:593) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:515) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:320) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:222) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:318) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:199) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.config.DependencyDescriptor.resolveCandidate(DependencyDescriptor.java:277) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.doResolveDependency(DefaultListableBeanFactory.java:1255) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.resolveDependency(DefaultListableBeanFactory.java:1175) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.ConstructorResolver.resolveAutowiredArgument(ConstructorResolver.java:857) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.ConstructorResolver.createArgumentArray(ConstructorResolver.java:760) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.ConstructorResolver.autowireConstructor(ConstructorResolver.java:218) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.autowireConstructor(AbstractAutowireCapableBeanFactory.java:1341) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1187) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:555) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:515) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:320) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:222) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:318) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:199) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.ConstructorResolver.instantiateUsingFactoryMethod(ConstructorResolver.java:392) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.instantiateUsingFactoryMethod(AbstractAutowireCapableBeanFactory.java:1321) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBeanInstance(AbstractAutowireCapableBeanFactory.java:1160) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:555) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:515) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:320) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:222) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:318) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:199) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.context.support.AbstractApplicationContext.getBean(AbstractApplicationContext.java:1105) ~[spring-context-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:867) ~[spring-context-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:549) ~[spring-context-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:141) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:744) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:391) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:312) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1215) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1204) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at com.frankmoley.lil.learningspring.LearningSpringApplication.main(LearningSpringApplication.java:16) ~[classes/:na]

2020-10-03 22:51:02.091  INFO 16776 --- [           main] o.hibernate.jpa.internal.util.LogHelper  : HHH000204: Processing PersistenceUnitInfo [
	name: default
	...]
2020-10-03 22:51:02.189  INFO 16776 --- [           main] org.hibernate.Version                    : HHH000412: Hibernate Core {5.3.12.Final}
2020-10-03 22:51:02.191  INFO 16776 --- [           main] org.hibernate.cfg.Environment            : HHH000206: hibernate.properties not found
2020-10-03 22:51:02.416  INFO 16776 --- [           main] o.hibernate.annotations.common.Version   : HCANN000001: Hibernate Commons Annotations {5.0.4.Final}
2020-10-03 22:51:02.574  INFO 16776 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2020-10-03 22:51:03.625 ERROR 16776 --- [           main] com.zaxxer.hikari.pool.HikariPool        : HikariPool-1 - Exception during pool initialization.

org.postgresql.util.PSQLException: FATAL: password authentication failed for user "postgres"
	at org.postgresql.core.v3.ConnectionFactoryImpl.doAuthentication(ConnectionFactoryImpl.java:520) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.core.v3.ConnectionFactoryImpl.tryConnect(ConnectionFactoryImpl.java:141) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.core.v3.ConnectionFactoryImpl.openConnectionImpl(ConnectionFactoryImpl.java:192) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.core.ConnectionFactory.openConnection(ConnectionFactory.java:49) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.jdbc.PgConnection.<init>(PgConnection.java:195) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.Driver.makeConnection(Driver.java:458) ~[postgresql-42.2.8.jar:42.2.8]
	at org.postgresql.Driver.connect(Driver.java:260) ~[postgresql-42.2.8.jar:42.2.8]
	at com.zaxxer.hikari.util.DriverDataSource.getConnection(DriverDataSource.java:136) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.PoolBase.newConnection(PoolBase.java:369) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.PoolBase.newPoolEntry(PoolBase.java:198) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.HikariPool.createPoolEntry(HikariPool.java:467) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.HikariPool.checkFailFast(HikariPool.java:541) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.pool.HikariPool.<init>(HikariPool.java:115) ~[HikariCP-3.2.0.jar:na]
	at com.zaxxer.hikari.HikariDataSource.getConnection(HikariDataSource.java:112) ~[HikariCP-3.2.0.jar:na]
	at org.hibernate.engine.jdbc.connections.internal.DatasourceConnectionProviderImpl.getConnection(DatasourceConnectionProviderImpl.java:122) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator$ConnectionProviderJdbcConnectionAccess.obtainConnection(JdbcEnvironmentInitiator.java:180) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.initiateService(JdbcEnvironmentInitiator.java:68) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.engine.jdbc.env.internal.JdbcEnvironmentInitiator.initiateService(JdbcEnvironmentInitiator.java:35) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.boot.registry.internal.StandardServiceRegistryImpl.initiateService(StandardServiceRegistryImpl.java:94) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.createService(AbstractServiceRegistryImpl.java:263) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.initializeService(AbstractServiceRegistryImpl.java:237) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.getService(AbstractServiceRegistryImpl.java:214) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.id.factory.internal.DefaultIdentifierGeneratorFactory.injectServices(DefaultIdentifierGeneratorFactory.java:152) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.injectDependencies(AbstractServiceRegistryImpl.java:286) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.initializeService(AbstractServiceRegistryImpl.java:243) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.service.internal.AbstractServiceRegistryImpl.getService(AbstractServiceRegistryImpl.java:214) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.boot.internal.InFlightMetadataCollectorImpl.<init>(InFlightMetadataCollectorImpl.java:179) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.boot.model.process.spi.MetadataBuildingProcess.complete(MetadataBuildingProcess.java:119) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.metadata(EntityManagerFactoryBuilderImpl.java:904) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.hibernate.jpa.boot.internal.EntityManagerFactoryBuilderImpl.build(EntityManagerFactoryBuilderImpl.java:935) ~[hibernate-core-5.3.12.Final.jar:5.3.12.Final]
	at org.springframework.orm.jpa.vendor.SpringHibernateJpaPersistenceProvider.createContainerEntityManagerFactory(SpringHibernateJpaPersistenceProvider.java:58) ~[spring-orm-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.createNativeEntityManagerFactory(LocalContainerEntityManagerFactoryBean.java:365) ~[spring-orm-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.buildNativeEntityManagerFactory(AbstractEntityManagerFactoryBean.java:391) ~[spring-orm-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.orm.jpa.AbstractEntityManagerFactoryBean.afterPropertiesSet(AbstractEntityManagerFactoryBean.java:378) ~[spring-orm-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean.afterPropertiesSet(LocalContainerEntityManagerFactoryBean.java:341) ~[spring-orm-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1837) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1774) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:593) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:515) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:320) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:222) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:318) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:199) ~[spring-beans-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.context.support.AbstractApplicationContext.getBean(AbstractApplicationContext.java:1105) ~[spring-context-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:867) ~[spring-context-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:549) ~[spring-context-5.1.10.RELEASE.jar:5.1.10.RELEASE]
	at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:141) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:744) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:391) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:312) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1215) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at org.springframework.boot.SpringApplication.run(SpringApplication.java:1204) ~[spring-boot-2.1.9.RELEASE.jar:2.1.9.RELEASE]
	at com.frankmoley.lil.learningspring.LearningSpringApplication.main(LearningSpringApplication.java:16) ~[classes/:na]

2020-10-03 22:51:03.626  WARN 16776 --- [           main] o.h.e.j.e.i.JdbcEnvironmentInitiator     : HHH000342: Could not obtain connection to query metadata : FATAL: password authentication failed for user "postgres"
2020-10-03 22:51:03.638  INFO 16776 --- [           main] org.hibernate.dialect.Dialect            : HHH000400: Using dialect: org.hibernate.dialect.PostgreSQL95Dialect
2020-10-03 22:51:03.658  INFO 16776 --- [           main] org.hibernate.type.BasicTypeRegistry     : HHH000270: Type registration [java.util.UUID] overrides previous : org.hibernate.type.UUIDBinaryType@50ec4bfc
2020-10-03 22:51:04.185  INFO 16776 --- [           main] j.LocalContainerEntityManagerFactoryBean : Initialized JPA EntityManagerFactory for persistence unit 'default'
2020-10-03 22:51:04.661  INFO 16776 --- [           main] o.s.s.concurrent.ThreadPoolTaskExecutor  : Initializing ExecutorService 'applicationTaskExecutor'
2020-10-03 22:51:04.731  WARN 16776 --- [           main] aWebConfiguration$JpaWebMvcConfiguration : spring.jpa.open-in-view is enabled by default. Therefore, database queries may be performed during view rendering. Explicitly configure spring.jpa.open-in-view to disable this warning
2020-10-03 22:51:04.764  INFO 16776 --- [           main] o.s.b.a.w.s.WelcomePageHandlerMapping    : Adding welcome page: class path resource [static/index.html]
2020-10-03 22:51:04.821  WARN 16776 --- [           main] ion$DefaultTemplateResolverConfiguration : Cannot find template location: classpath:/templates/ (please add some templates or check your Thymeleaf configuration)
2020-10-03 22:51:05.014  INFO 16776 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8080 (http) with context path ''
2020-10-03 22:51:05.018  INFO 16776 --- [           main] c.f.l.l.LearningSpringApplication        : Started LearningSpringApplication in 7.206 seconds (JVM running for 7.772)

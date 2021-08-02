# ISBuilder project

### Начало

- Склонировать основной проект

```bash
git clone https://gitlab.rusoft.tech/sogis/ISBuilder.git
```

> Либо по [ssh](https://docs.gitlab.com/ee/ssh/)

```bash
git clone ssh://git@gitlab.rusoft.tech:2224/sogis/isbuilder.git
```

- Склонировать сабмодули

```bash
git submodule update --init --recursive
```

- Установить [java](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- Установить [maven](https://maven.apache.org/install.html)
- Запустить сборку проекта

```bash
Весь проект:
mvn clean package (-DskipTests=true)
Один модуль:
mvn package -pl core -am -DskipTests=true
```

- Будет создана директория `target`, в ней можно найти собранные артефакты, отчет о покрытии, документацию к rest-api
- Отчет по покрытию тестами можно найти в директории `target/site/jacoco/index.html`
- Документацию к rest-api можно найти в `target/rest-api/index.html`

### Сборка

- Проект содержит сабмодули, подтянуть их можно командой `git submodule update --init --recursive`
- Собрать можно `mvn package -Pfull`. Команда соберет проект, запустит unit-тесты, сформирует документацию к API

> -Pfull - собрать вместе с интерфейсом, если интерфейс не нужен - можно запустить без этого параметра


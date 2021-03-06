# vuex-boilerplate
> **vuex-boilerplate** - это стартовый шаблон для разработки SPA приложений на Vue.js. Здесь настроена система сборки проекта с помощью [**vue-cli 3**](https://cli.vuejs.org/ru/), а так же работает тестовый сервер на [**Node.js**](https://nodejs.org/en/) с API и подключением базы данных [**MongoDB**](https://www.mongodb.com) 
## Клонирование и запуск проекта
```bash
# Перейдите в папку с проектами и выполните команду
$ git clone https://gitlab.s256.ru/ulyanov/vuex-boilerplate.git

# Перейдите в папку клонированного проекта
$ cd vuex-boilerplate

# Установите зависимости проекта
$ npm install
# ИЛИ
$ yarn install
```

## Работа с DEV окружением
```bash
# Для более удобной работы с NPM командами установите менеджер команд NTL
$ npm install -g ntl
# ИЛИ
$ yarn global add ntl

# Презагрузите консоль и воспользуйтесь короткой командой
$ ntl
# Вам станет доступен интерактивный выбор NPM команд с помощью клавиш "up", "down"

# Либо воспользуйтесь предустановленными командами:
# Запуск девсервера + девсервера Node&MongoDB + девсервера с документацией проекта
$ npm run dev
# ИЛИ
$ yarn dev 

# Запуск линтера
$ npm run lint
# ИЛИ
$ yarn lint

# Запуск девсервера для правки документации
$ npm run docs:dev
# ИЛИ
$ yarn docs:dev
```

## Логика работы с DEV-хостами
После выполнения команды `$ npm run dev` будет запущено одновременно два сервера:  
* [http://localhost:8080/](http://localhost:8080/) - здесь будет запущено само приложение
* [http://localhost:6006/](http://localhost:6006/) - здесь будет запущен сервер с тестовым API

## Работа с BUILD окружением
```bash
# Билд проекта + полная перезапись папки dist 
# + минификация ресурсов, маппинг и разделение на бандлы
$ npm run build
# ИЛИ
$ yarn build

# После билда проекта перейдите в папку с подготовленными файлами
$ cd dist

# Внутри папки можете запустить сервер с продакшен-файлами 
# для проверки корректности сборки
# Сервер работает через сервис browser-sync + девсервер Node&MongoDB 
$ ../node_modules/browser-sync/dist/bin.js start --server --files 'css/*.css,js/*.js,html/*.html,*.*' & ../node_modules/.bin/nodemon ../server/app.js

# Также после правки документации вы можете выполнить билд приложения
# которое будет сохранено в .vuepress/dist
# и размещать любым удобным способом онлайн

# Проверить корректность билда документации можно следующим образом:
#из корневой папки проекта перейдите в папку билда
$ cd .vuepress/dist

# запустите девсервер из это папки
$ ../../node_modules/browser-sync/dist/bin.js start --server --files 'css/*.css,js/*.js,html/*.html,*.*'
```

## Главы документации

В этом проекте есть папка `docs` с более подробной информацией o:

1.  [Архитектура проекта](docs/architecture.md)

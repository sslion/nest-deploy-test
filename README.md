<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Project setup

```bash
$ npm install
```

## Compile and run the project

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Run tests

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ npm install -g @nestjs/mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.

## Resources

Check out a few resources that may come in handy when working with NestJS:

- Visit the [NestJS Documentation](https://docs.nestjs.com) to learn more about the framework.
- For questions and support, please visit our [Discord channel](https://discord.gg/G7Qnnhy).
- To dive deeper and get more hands-on experience, check out our official video [courses](https://courses.nestjs.com/).
- Deploy your application to AWS with the help of [NestJS Mau](https://mau.nestjs.com) in just a few clicks.
- Visualize your application graph and interact with the NestJS application in real-time using [NestJS Devtools](https://devtools.nestjs.com).
- Need help with your project (part-time to full-time)? Check out our official [enterprise support](https://enterprise.nestjs.com).
- To stay in the loop and get updates, follow us on [X](https://x.com/nestframework) and [LinkedIn](https://linkedin.com/company/nestjs).
- Looking for a job, or have a job to offer? Check out our official [Jobs board](https://jobs.nestjs.com).

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://twitter.com/kammysliwiec)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).

## Настройка автодеплоя

Отличный вопрос! Разберем весь процесс максимально подробно. Я буду предполагать, что у вас есть:

- Локальный компьютер с установленными Node.js, NestJS CLI и Git
- Сервер с ОС Linux (например, Ubuntu 20.04/22.04) с доступом по SSH
- Аккаунт на GitHub/GitLab/Bitbucket

Весь процесс разделим на 4 больших этапа:

1. **Локальная подготовка проекта и Git**
2. **Настройка удаленного репозитория**
3. **Подготовка сервера**
4. **Настройка автодеплоя**

---

## Этап 1: Локальная подготовка проекта и Git

### Шаг 1.1: Инициализация Git в проекте

```bash
# Переходим в папку вашего Nest.js проекта
cd /path/to/your/nest-project

# Инициализируем локальный репозиторий Git
git init
```

**Что происходит:** Команда `git init` создает в папке проекта скрытую директорию `.git`, где будет храниться вся история изменений и служебная информация.

### Шаг 1.2: Создаем .gitignore

Перед первым коммитом обязательно создайте файл `.gitignore`:

```bash
# Создаем файл .gitignore
touch .gitignore

# Открываем его для редактирования (можно через любой текстовый редактор)
nano .gitignore
```

Добавьте туда примерно такое содержимое:

```
# Зависимости
node_modules/
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Логи
logs
*.log

# Runtime data
pids
*.pid
*.seed
*.pid.lock

# Coverage directory used by tools like istanbul
coverage/

# Environment variables
.env
.env.local
.env.production

# IDE
.vscode/
.idea/
*.swp
*.swo

# Build output
dist/
build/
```

**Почему это важно:** Файл `.gitignore` указывает Git, какие файлы и папки НЕ нужно отслеживать. Мы исключаем:

- `node_modules/` - зависимости можно установить через `npm install`
- `.env` - файлы с паролями и ключами
- `dist/` - скомпилированные файлы (генерируются при сборке)
- файлы редакторов и временные файлы

### Шаг 1.3: Первый коммит

```bash
# Добавляем все файлы (кроме тех, что в .gitignore) в staging area
git add .

# Проверяем, что будет закоммичено
git status

# Создаем первый коммит с описанием
git commit -m "Initial commit: Nest.js project structure"
```

**Объяснение команд:**

- `git add .` - добавляет все измененные файлы в "промежуточную область"
- `git status` - показывает текущее состояние репозитория
- `git commit -m "сообщение"` - создает коммит (снимок текущего состояния) с комментарием

---

## Этап 2: Настройка удаленного репозитория

### Шаг 2.1: Создаем репозиторий на GitHub

1. Зайдите на GitHub.com
2. Нажмите "+" в右上ом углу → "New repository"
3. Введите название (например, "my-nest-app")
4. **НЕ** добавляйте README, .gitignore или license - они у нас уже есть
5. Нажмите "Create repository"

### Шаг 2.2: Привязываем локальный репозиторий к удаленному

```bash
# Добавляем удаленный репозиторий (замените username и repo-name на свои)
git remote add origin https://github.com/username/repo-name.git

# Отправляем код на GitHub
git push -u origin main
# или если у вас ветка называется master:
git push -u origin master
```

**Что делают команды:**

- `git remote add origin URL` - добавляет удаленный репозиторий под именем "origin"
- `git push -u origin main` - отправляет код в ветку "main" и устанавливает связь между локальной и удаленной веткой

---

## Этап 3: Подготовка сервера

### Шаг 3.1: Подключаемся к серверу

```bash
# Подключаемся к серверу по SSH (замените your-user и your-server-ip)
ssh your-user@your-server-ip
```

### Шаг 3.2: Устанавливаем необходимое ПО на сервер

```bash
# Обновляем список пакетов
sudo apt update && sudo apt upgrade -y

# Устанавливаем Node.js (пример для Ubuntu)
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# Устанавливаем PM2 - процесс менеджер для Node.js приложений
sudo npm install -g pm2

# Устанавливаем Git
sudo apt install git -y

# Устанавливаем nginx (для проксирования запросов)
sudo apt install nginx -y

# Устанавливаем firewall (если не установлен)
sudo apt install ufw -y
sudo ufw allow OpenSSH
sudo ufw allow 'Nginx Full'
sudo ufw enable
```

**Объяснение:**

- **Node.js** - среда выполнения для нашего Nest.js приложения
- **PM2** будет управлять нашим приложением (перезапускать при падении, логировать и т.д.)
- **nginx** будет принимать HTTP запросы и проксировать их на наше приложение
- **ufw** - firewall для безопасности

### Шаг 3.3: Настраиваем пользователя и рабочую директорию

```bash
# Создаем пользователя для приложения (рекомендуется для безопасности)
sudo adduser --disabled-password --gecos "" appuser

# Переключаемся на пользователя appuser
sudo su - appuser

# Создаем структуру папок
mkdir -p ~/app ~/logs
```

### Шаг 3.4: Клонируем репозиторий на сервер

```bash
# Клонируем проект (замените на ваш URL)
git clone https://github.com/username/repo-name.git ~/app
```

---

## Этап 4: Настройка автодеплоя

### Шаг 4.1: Настройка Webhook на GitHub

1. Зайдите в ваш репозиторий на GitHub
2. Перейдите в Settings → Webhooks → Add webhook
3. В "Payload URL" введите: `http://your-server-ip:5000/webhook`
4. Content type: `application/json`
5. Secret: придумайте сложную строку (запомните ее)
6. Выберите "Just the push event"
7. Отметьте "Active" и нажмите "Add webhook"

### Шаг 4.2: Создаем скрипт деплоя на сервере

На сервере создаем файл `~/scripts/deploy.sh`:

```bash
#!/bin/bash

# Логируем начало деплоя
echo "=== Starting deploy at $(date) ===" >> ~/logs/deploy.log

# Переходим в папку приложения
cd ~/app

# Получаем последние изменения из Git
git fetch --all
git reset --hard origin/main

# Устанавливаем зависимости
npm install

# Собираем приложение (если это TypeScript проект)
npm run build

# Перезапускаем приложение через PM2
pm2 restart my-nest-app

# Логируем успешное завершение
echo "=== Deploy completed at $(date) ===" >> ~/logs/deploy.log
```

Делаем скрипт исполняемым:

```bash
chmod +x ~/scripts/deploy.sh
```

### Шаг 4.3: Создаем простое Node.js приложение для обработки webhook

На сервере создаем `~/webhook/webhook-listener.js`:

```javascript
const http = require('http');
const crypto = require('crypto');
const { exec } = require('child_process');

const SECRET = 'your-github-webhook-secret'; // Тот же секрет, что в GitHub
const PORT = 5000;

http
  .createServer((req, res) => {
    if (req.url === '/webhook' && req.method === 'POST') {
      let body = '';

      req.on('data', (chunk) => {
        body += chunk.toString();
      });

      req.on('end', () => {
        // Проверяем подпись для безопасности
        const signature = req.headers['x-hub-signature-256'];
        const hmac = crypto.createHmac('sha256', SECRET);
        const digest = 'sha256=' + hmac.update(body).digest('hex');

        if (signature === digest) {
          // Запускаем скрипт деплоя
          exec('~/scripts/deploy.sh', (error, stdout, stderr) => {
            if (error) {
              console.error(`Deploy error: ${error}`);
            }
          });

          res.writeHead(200, { 'Content-Type': 'application/json' });
          res.end(JSON.stringify({ message: 'Deploy started' }));
        } else {
          res.writeHead(401, { 'Content-Type': 'application/json' });
          res.end(JSON.stringify({ message: 'Invalid signature' }));
        }
      });
    } else {
      res.writeHead(404);
      res.end();
    }
  })
  .listen(PORT);

console.log(`Webhook listener running on port ${PORT}`);
```

### Шаг 4.4: Запускаем все через PM2

Создаем файл `~/ecosystem.config.js`:

```javascript
module.exports = {
  apps: [
    {
      name: 'my-nest-app',
      cwd: '/home/appuser/app',
      script: 'npm',
      args: 'start',
      env: {
        NODE_ENV: 'production',
        PORT: 3000,
      },
    },
    {
      name: 'webhook-listener',
      cwd: '/home/appuser/webhook',
      script: 'webhook-listener.js',
      env: {
        NODE_ENV: 'production',
      },
    },
  ],
};
```

Запускаем:

```bash
pm2 start ecosystem.config.js
pm2 startup  # Настраиваем автозапуск при загрузке сервера
pm2 save     # Сохраняем текущие процессы
```

### Шаг 4.5: Настраиваем nginx

Создаем конфиг `/etc/nginx/sites-available/my-nest-app`:

```nginx
server {
    listen 80;
    server_name your-server-ip;  # или ваше доменное имя

    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_cache_bypass $http_upgrade;
    }
}
```

Активируем конфиг:

```bash
sudo ln -s /etc/nginx/sites-available/my-nest-app /etc/nginx/sites-enabled/
sudo nginx -t  # Проверяем конфигурацию
sudo systemctl restart nginx
```

---

## Проверка работы

Теперь, когда вы делаете изменения в коде на локальной машине:

```bash
# Делаем изменения...
git add .
git commit -m "Some feature"
git push
```

После push на GitHub автоматически:

1. GitHub отправляет webhook на ваш сервер
2. Webhook-listener проверяет подпись и запускает deploy.sh
3. Скрипт обновляет код, устанавливает зависимости и перезапускает приложение

---

## Альтернативный упрощенный подход: GitHub Actions

Если webhook кажется сложным, можно использовать GitHub Actions. Создайте файл `.github/workflows/deploy.yml` в репозитории:

```yaml
name: Deploy to Server

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Deploy to server
        uses: appleboy/ssh-action@master
        with:
          host: ${{ secrets.SERVER_HOST }}
          username: ${{ secrets.SERVER_USER }}
          key: ${{ secrets.SSH_PRIVATE_KEY }}
          script: |
            cd /home/appuser/app
            git pull origin main
            npm install
            npm run build
            pm2 restart my-nest-app
```

В настройках репозитория GitHub добавьте Secrets:

- `SERVER_HOST` - IP вашего сервера
- `SERVER_USER` - appuser
- `SSH_PRIVATE_KEY` - приватный SSH ключ для доступа к серверу

---

Это полная инструкция по настройке CI/CD пайплайна для начинающего. Начните с основного подхода, а когда освоитесь - переходите к GitHub Actions, который считается более современным и удобным подходом.

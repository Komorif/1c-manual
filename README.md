Гайд как создать такой же сайт

(1) Создание проекта

Создаем пустую папку и выполняем в терминале данную команду

```bash
git clone https://github.com/jackyzha0/quartz.git
```

Переименуем папку в какую мы хотим

```bash
cd наше-переименованное-название
npm i (npm install)
npx quartz create (выбираем далее что нас интересует)
```

При ошибке "выполнение сценариев отключено в этой системе":

```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

При ошибке "Недостаточно прав доступа для выполнения этой операции":

```bash
Set-ExecutionPolicy RemoteSigned - ASet-ExecutionPolicy RemoteSigned
```

(2) Привязка к github

```bash
git remote -v
git remote rm origin
git remote add origin https://... (ссылка по https)
npx quartz sync --no-pull
```

(3) Выпуск в продакшен

Заходим в GitHub Desktop. Делаем clone нашего репозитория который мы создали на шаге (2). Затем переходим в папку с клонированным репозиторием создаем по пути .github/workflows папку deploy.yml. Затем переходим по [ссылке](https://quartz.jzhao.xyz/hosting) и копируем код из блока GitHub Pages.

После сохранения изменений в нашем репозитории появился файл deploy.yml заходим в настройки проекта и нажимаем Pages->GitHub Actions

Опционально:
Каждый раз изменяя контент заходим в GitHub Desktop и делаем комиты и push в ветку origin




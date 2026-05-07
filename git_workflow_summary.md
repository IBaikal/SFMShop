# Git Workflow для проекта SFMShop

## Использованные команды Git

- git init — инициализация репозитория
- git add — добавление файлов в staging area
- git commit -m — создание коммита
- git branch — просмотр и создание веток
- git checkout -b — создание и переключение на новую ветку
- git checkout — переключение между ветками
- git merge — слияние веток
- git rebase — перебазирование ветки
- git push origin — отправка в удаленный репозиторий
- git pull origin — получение изменений
- git remote add — привязка удаленного репозитория
- git status — проверка состояния
- git log --oneline --graph --all — визуализация истории
- git log --stat — статистика изменений
- git diff — сравнение веток
- git show — просмотр коммита
- git restore — откат изменений
- git stash / git stash pop — временное сохранение изменений

## Созданные ветки

- main — основная ветка, стабильный код
- feature/add-discount-system — система скидок
- feature/add-inventory-management — управление складом
- feature/add-shipping — расчет доставки
- feature/add-email-validation — валидация email
- feature/add-logging — система логирования
- feature/add-caching — система кэширования
- feature/test-conflict — отработка конфликтов
- feature/test-stash — отработка git stash
- feature/test-rebase — отработка git rebase

## Разрешенные конфликты

- Конфликт в src/models/product.py при слиянии feature/test-conflict в main
- Конфликт в src/models/product.py при слиянии main в feature/add-shipping
- Оба конфликта разрешены вручную с сохранением всех методов

## Как организован workflow

1. Новые функции — в отдельных feature-ветках от main
2. Коммиты с осмысленными сообщениями на русском
3. Перед PR ветка обновляется из main (merge или rebase)
4. Конфликты разрешаются вручную
5. Ветка пушится на GitHub и создается Pull Request
6. После проверки PR сливается в main

## Стратегия работы с ветками

- main — только проверенный код
- feature/* — новые функции
- Ветки короткоживущие, по одной задаче на ветку
- Перед PR — синхронизация с main
- Конфликты — разрешать вручную, сохраняя все изменения
EOF
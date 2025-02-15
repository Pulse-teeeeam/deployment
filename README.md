# ❤ PULSE TEAM

> ### 🔑 **ТОЛЬКО ДЛЯ ПРОВЕРЯЮЩИХ**  
> Авторизация в Container Registry `(Read Only)`:  
> Команда - **docker login cr.selcloud.ru**  
> Логин - **token**  
> Пароль - **CRgAAAAAF0BhHp7mZ42awvN0id-mlt2LSg9CVLXL**  
> **TODO:** Удалить пользователя после хакатона  

## ℹ️ Информация
Для деплоя используется **Kubernetes**, также мы используем **ci/cd** в **GitHub Actions** что-бы быстро деплоить `(Можете посмотреть в репозиториях)`  
Ссылка на сайт — **pulse-work.ru**

## 📦 Контейнеры 
#### Backend

- Ссылка — https://github.com/Pulse-teeeeam/backend
- Расположение — `cr.selcloud.ru/pulse-teal/backend`
- Технологии:

![DJANGO](https://img.shields.io/badge/-Django-black?style=for-the-badge&logo=django)
![GraphQL](https://img.shields.io/badge/-GraphQL-black?style=for-the-badge&logo=GraphQL)
![AmazonS3](https://img.shields.io/badge/-S3-black?style=for-the-badge&logo=AmazonS3)

#### Frontend

- Ссылка — https://github.com/Pulse-teeeeam/frontend
- Расположение — `cr.selcloud.ru/pulse-teal/frontend`
- Технологии:

![NEXTJS](https://img.shields.io/badge/-NextJS-black?style=for-the-badge&logo=next.js)
![tailwindcss](https://img.shields.io/badge/-tailwindcss-black?style=for-the-badge&logo=tailwindcss)

## 📄 Развёртывание в Kubernetes  

1. Создание namespace
```bash
kubectl create namespace pulse
```

2. Создание secret для доступа к Container Registry
```bash
kubectl create secret docker-registry cr-secret --docker-server=cr.selcloud.ru --docker-username=token --docker-password=ТОКЕН --namespace=pulse
```

3. Запуск приложений

```bash
kubectl apply -f kubernetes/ПУТЬ
```

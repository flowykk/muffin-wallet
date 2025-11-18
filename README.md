# Описание выполненной работы

Проект состоит из двух микросервисов: `muffin-wallet` и `muffin-currency`. Для деплоя в Kubernetes используется Helm.

### Запуск

Основные инструкции прописаны в файлах `NOTES.txt` и будут выводиться в терминале после установки соответствующего релиза

```bash
# Установка чартов
helm install muffin-currency helm-muffin-currency/
helm install muffin-wallet helm-muffin-wallet/

# Проверяем установленные релизы
helm list
kubectl get pods
```

## Ещё разные команды

```bash
# Обновить релиз с новыми правками
helm upgrade muffin-wallet helm-muffin-wallet/ --set replicaCount=5

# Удалить релизы
helm uninstall muffin-wallet
helm uninstall muffin-currency
```

## Database structure

![ER](https://www.plantuml.com/plantuml/svg/5Smx4W8X303GtbFe0IHZQxLNYIG8Co7iv2FNLwlNlSC3BNBAvJQqIX9VUyJfJm33NTuZUhxIsUhIO8rIrmGar8Ui3yniRUXzemW763U7paWE4uS2hGfivVpl1olz_080)

## Sequence Diagram

![SD](https://www.plantuml.com/plantuml/svg/5Sqn4W8X30NGtbFe0IHZQxLNYV0HPa9OIU9UNxTwvTlCUNaCkTowPec2QtFVxKcq-4ZlxYrUOLXvgaCzvJc82-j3vfT6rDhrVh08d1QgKGCNey5TgSnCXaz0Cz9-7Xkq_Fq1)

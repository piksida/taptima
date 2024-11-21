# Инструкция

Ссылки на Docker-образы:
* [Backend image](https://hub.docker.com/layers/evagertseva/test/backend/images/sha256-3c9e8b7c5b6a7c2d704aca1fca6ba79980b1c02cea5e8712acf58ffdfa84c625?context=repo)
* [Frontend image](https://hub.docker.com/layers/evagertseva/test/frontend/images/sha256-ef872920566202cc069dc9e400f1952aa12dab83bb799dde32fb9e4d0798df64?context=explore)
Запуск приложения:
* Манифесты хранятся в папке k8s. Namespace.yml создает namespace 
questioannire, в который деплоятся остальные манифесты.
* Для работы ингресса требуется воспользоваться командой minikube addons 
enable ingress. Далее sudo minikube tunnel. Для открытия приложения в 
браузере требуется внести в /ect/hosts 127.0.0.1 questionnaire.local

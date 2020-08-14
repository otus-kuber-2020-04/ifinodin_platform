# ifinodin_platform
ifinodin Platform repository

## HW2: K8S INTRO
1. Разберитесь почему все pod в namespace kube-system
восстановились после удаления.
- kube-apiserver восстанавливает kubelet, используя манифесты кластера
- прочие поды восстанавливаются, если используется replication-controller
- "голые" поды не восстанавливаются

2. Создан Dockerfile, описывающий образ вебсервера на основе nginx:
Build:
- docker build -t ifinodin/otus-hw2:0.3 .
Push to repo:
- docker push ifinodin/otus-hw2:0.3

3. Создан манифест web-pod.yaml, использующийся для запуска пода.
- После проверки вебсервер отдает index.html с logo 'express 42'

4. Склонирован и запущен frontend hs, выполнен фикс - добавлены env. 
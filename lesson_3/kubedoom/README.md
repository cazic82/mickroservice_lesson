Для запуска приложения kubedoom делаем следующие шаги:
1. на машину ставим Docker
2. ставим kubectl
3. ставим minikube
4. запускаем minikube:
    $ minikube start
5. запускаем манифесты:
    $ kubectl apply -f https://raw.githubusercontent.com/cazic82/mickroservice_lesson/main/lesson_3/kubedoom/namespace.yaml
    $ kubectl apply -f https://raw.githubusercontent.com/cazic82/mickroservice_lesson/main/lesson_3/kubedoom/ServiceAccount.yaml
    $ kubectl apply -f https://raw.githubusercontent.com/cazic82/mickroservice_lesson/main/lesson_3/kubedoom/ClusterRoleBinding.yaml
    $ kubectl apply -f https://raw.githubusercontent.com/cazic82/mickroservice_lesson/main/lesson_3/kubedoom/Deployment.yaml
6. прокидываем порты:
    $ kubectl port-forward [имя рабочего POD, скобки убираем] -n kubedoom 5901:5900
7. сатавим vnc клиент (vncviewer)
8. запускаем vncviewer и получаем доступ к рабочему приложению:
    $ vncviewer viewer localhost:5901
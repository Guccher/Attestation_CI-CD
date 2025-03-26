CI/CD. Семинар 04. Troubleshooting (диагностика и решение проблем в CI/CD)
Задача
Сделать локальный шаблон CI и отдельный репозиторий с шаблонами, подключить их к своему основному репозиторию через include

Решение
Создан локальный файл local-smoke-tests.gitlab-ci.yml

smoke-test-job:
  script: echo "SMOKE"
Создан основной файл .gitlab-ci.yml

include:
  - local: local-smoke-tests.gitlab-ci.yml
#  - remote: https://github.com/Valinetsky/-CI-CD_Seminar04/blob/main/remote-included-file.yml
  - remote: https://gitlab.com/ci-cd7655047/5/-/raw/main/remote-included-file.yml
Файл с аналогичным содержанием есть в этом репозитории: remote_included-file.yml

Repository Seminar04 repository
![image](https://github.com/user-attachments/assets/05c22e1c-36ae-41ed-adc0-bf68884eb5df)


Remote included file job remote included file job
![image](https://github.com/user-attachments/assets/a8d493c3-f9b6-4971-ad54-e7d09d0d5948)

Pipeline passed pipeline passed
![image](https://github.com/user-attachments/assets/7f65dba6-f29f-4eb3-90e1-d0f8c00b2a0b)


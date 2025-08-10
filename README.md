
# Домашнее задание к занятию 11 «Teamcity»

## Подготовка к выполнению

Через Terraform создана инфраструктура для выполнения задания.

https://github.com/DioRoman/09-ci-05-teamcity

<img width="2451" height="387" alt="Снимок экрана 2025-08-10 165216" src="https://github.com/user-attachments/assets/6e7ad0d4-bcf1-4192-8e16-22fca98182b1" />

## Основная часть

1. Создайте новый проект в teamcity на основе fork.
2. Сделайте autodetect конфигурации.
3. Сохраните необходимые шаги, запустите первую сборку master.
4. Поменяйте условия сборки: если сборка по ветке `master`, то должен происходит `mvn clean deploy`, иначе `mvn clean test`.

<img width="1979" height="765" alt="Снимок экрана 2025-08-10 011107" src="https://github.com/user-attachments/assets/78e7c207-f5de-4900-8691-59e2fa031072" />
  
5. Для deploy будет необходимо загрузить [settings.xml](./teamcity/settings.xml) в набор конфигураций maven у teamcity, предварительно записав туда креды для подключения к nexus.
6. В pom.xml необходимо поменять ссылки на репозиторий и nexus.
7. Запустите сборку по master, убедитесь, что всё прошло успешно и артефакт появился в nexus.

<img width="2510" height="767" alt="Снимок экрана 2025-08-09 195816" src="https://github.com/user-attachments/assets/df93f677-f74b-467d-bfb7-d15b343cf824" />
   
8. Мигрируйте `build configuration` в репозиторий.

<img width="1979" height="957" alt="Снимок экрана 2025-08-10 000317" src="https://github.com/user-attachments/assets/21f3a45a-233c-4cb9-94bd-81748deb318e" />

<img width="1679" height="1157" alt="Снимок экрана 2025-08-10 000351" src="https://github.com/user-attachments/assets/2903ae55-863b-4b02-8488-bcde74b978d3" />

<img width="1076" height="844" alt="Снимок экрана 2025-08-09 195932" src="https://github.com/user-attachments/assets/16d590d7-d96c-484d-ba6b-47ca959b8fe8" />

9. Создайте отдельную ветку `feature/add_reply` в репозитории.

10. Напишите новый метод для класса Welcomer: метод должен возвращать произвольную реплику, содержащую слово `hunter`.
11. Дополните тест для нового метода на поиск слова `hunter` в новой реплике.
12. Сделайте push всех изменений в новую ветку репозитория.
13. Убедитесь, что сборка самостоятельно запустилась, тесты прошли успешно.

<img width="1990" height="356" alt="Снимок экрана 2025-08-10 002817" src="https://github.com/user-attachments/assets/aed500c8-b02c-4292-b149-f0c47cfa73aa" />

14. Внесите изменения из произвольной ветки `feature/add_reply` в `master` через `Merge`.
15. Убедитесь, что нет собранного артефакта в сборке по ветке `master`.
16. Настройте конфигурацию так, чтобы она собирала `.jar` в артефакты сборки.

<img width="1662" height="868" alt="Снимок экрана 2025-08-10 013741" src="https://github.com/user-attachments/assets/b3bfc658-938b-4752-9f65-fbe0f45031e1" />
    
17. Проведите повторную сборку мастера, убедитесь, что сбора прошла успешно и артефакты собраны.

<img width="930" height="554" alt="Снимок экрана 2025-08-10 013816" src="https://github.com/user-attachments/assets/183d2d22-ab7b-427d-8081-0830379eead9" />

18. Проверьте, что конфигурация в репозитории содержит все настройки конфигурации из teamcity.
19. В ответе пришлите ссылку на репозиторий.

https://github.com/DioRoman/example-teamcity


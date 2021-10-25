# Решение домашнего задание к занятию «1.1. Введение в DevOps»

## Задание №1 - Подготовка рабочей среды

1. [main.py](https://github.com/anatolben/DEVSYS-PDC-2/blob/main/01-intro-01/main.py)
   ![main.py](https://i.imgur.com/BICkGXK.png)

2. [netology.jsonnet](https://github.com/anatolben/DEVSYS-PDC-2/blob/main/01-intro-01/netology.jsonnet)
   ![netology.jsonnet](https://i.imgur.com/Xv4pY6s.png)

3. [netology.tf](https://github.com/anatolben/DEVSYS-PDC-2/blob/main/01-intro-01/netology.tf)
   ![netology.tf](https://i.imgur.com/80CxU16.png)

4. [netology.yaml](https://github.com/anatolben/DEVSYS-PDC-2/blob/main/01-intro-01/netology.yaml)
   ![netology.yaml](https://i.imgur.com/E6lhvvV.png)

5. [netology.md](https://github.com/anatolben/DEVSYS-PDC-2/blob/main/01-intro-01/netology.md?plain=1)
   ![netology.md](https://i.imgur.com/7Ir2buj.png)

6. [netology.sh](https://github.com/anatolben/DEVSYS-PDC-2/blob/main/01-intro-01/netology.sh)
   ![netology.sh](https://i.imgur.com/PSFsCRj.png)


## Задание №2 - Описание жизненного цикла задачи (разработки нового функционала)

1. Клиент >(задача)> PM  
2. PM >(задачи на создание:  
    + dev среды для DevTeam;  
    + alpha среды для QATeam;  
    + stage[beta] среды для QATeam, PM;  
    + автоматизации релизов на production по схеме: бекап-релиз-откат_релиза)> DevOps  
3. PM >(задача на реализацию кода и тестов)> DevTeam  
4. DevOps >(создание сред)> DevTeam, QATeam, PM  
5. DevTeam >(создание кода и тестов на dev)>(мерж на alpha)> QATeam  
6. QATeam >(успех проверки alpha)> PM || QATeam >(неуспех проверки alpha)>(итерация разработки)> DevTeam п.5  
7. PM >(задача на мерж в beta)> DevTeam  
8. DevTeam >(задача на проверку beta)> QATeam  
9. QATeam >(успех проверки beta)> PM || QATeam >(неуспех проверки beta, итерация разработки)> DevTeam п.5, QATeam п.6, DevOps п.2  
10. PM >(апрув, презентация beta)> Клиент  
11. PM >(успех презентации beta, задача на релиз)> DevOps || PM >(неуспех презентации beta, итерация разработки)> DevTeam п.5, QATeam п.6,9, DevOps п.2  
12. DevOps >(релиз production)> QATeam, PM  
13. DevOps, QATeam, PM >(успех релиза production)> Клиент || DevOps, QATeam, PM >(неуспех релиза production)>(откат до исходного состояния, итерация разработки)> DevTeam п.5, QATeam п.6,9, DevOps п.2  
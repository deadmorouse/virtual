Задача 1:  

Полная (аппаратная) виртуализация  -  повторяет (эмулирует) физический компьютер.При полной виртуализации немодифицированная ОС работает так же, как если бы она не была виртуализирована, а вызовы ОС перехватываются и транслируются с использованием двоичного  преобразования. Обеспечивается изоляция гостевой ОС.  
  
Паравиртуализация  -  гостевые ОС оптимизированны для работы с гипервизором и  они "знают", что виртуализируются. В отличие от полной виртуализации в паравиртуализации присутствует возможность прямого использования гостевой ОС аппаратных ресурсов хоста.   

Виртуализация на уровне ОС - виртуализируется пользовательское окружение ОС.  
  

Задача 2: 

1) Высоконагруженная база данных, чувствительная к отказу - для размещения  можно использовать  
 1.1 Физический серевер, т.к. виртуализация снижает производительность в части утилизации I/O  
 1.2 Оптимизированная паравиртуализация (инфраструктура), обеспечивающая преимущества виртуализации.

2) Различные web-приложения - для размещения можно использовать  виртуализацию уровня ОС. Дает приемущества при разработке и эксплуатации приложений.


3) Windows системы для использования Бухгалтерским отделом - для размещения можно использовать  паравиртуализацию,так как  представляет облегчение миграции и бекапирования.


4) Системы, выполняющие высокопроизводительные расчеты на GPU - для размещения можно использовать  физические сервера т.к. виртуализация может негативно влиять на эффективность использования вычислительных ресурсов.


Задача 3:

1) 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.  
   Для данной задачи я бы предпочел использовать систему Hyper-V, в связи с приемущественностью Windows. Также Hyper-V имеет все возможности указанные в сценарии.
2) Требуется наиболее производительное бесплатное open source решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.  
   Для данной задачи могут подойти Xen, KVM , Proxmox VE. Все зависит от выполняемых операций, показатели их производительность зависит от выполняемых задач.
3) Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows инфраструктуры.
   Для данной задачи Microsoft Hyper-V Server имеет наибольшую совместимость с Windows системами. Также альтернативой может служить ProxmoxVE или Xen.

4) Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.  
   Для данной задачи Docker - решение виртуализации на уровне ОС, которое имеет наибольшую скорость развёртывания.

Задача 4:  

Нюансы гетерогенной среды виртуализации:

1) Высокий порог знаний  в части эксплуатации разного ПО виртуализации
2) усложнение операций по переносу и масштабированию виртуальных машин между различными средами
3) увелечение операционных расходов в случае использования нескольких проприетарных систем управления виртуализацией  
   
Необходимость создания гетерогенной среды может исходить из предложенных задач:  
1) предоставления услуг IaaS и инфраструктурных облачных сервисов со структурой виртуализационных платформ (которая предназначена для диверсификации);
2) необходимость распределения аппаратных ресурсов посредством полной виртуализации и облегчения задач размещения/развёртывания ПО посредством виртуализации на уровне ОС.
   

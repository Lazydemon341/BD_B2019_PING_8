### Practice  #1 DataBases
### Архаров Дмитрий Павлович БПИ198


1. Предложите список функциональных требований для проекта.

	- Размещение и поддержка цикла жизни каждого аукциона на товар в течении заданного времени размещения ставок.
	- Возможность поставить ставку на аукционе.
	- Определние победителя аукциона и поддержка обязательств по оплате и доставке товара.
	- Стркоа поиска подходящего аукциона, куда пользователь может ввести тег или название продукта, для поиска подходящего ему аукциона.
	- Система предлагает покупателю подходящие ему аукционы (в виде предложенных вариантов) на основе истории его покупок
	- Система отслеживания рейтинга продавца, можно ли ему доверять, основана на статистике доставленных продуктов.
	- 
	
2. Определите роли пользователей и действия для каждой роли.  
    
    Роли: Продавец, Покупатель.
    
	- Продавец создаёт новые аукционы, заполняя информацию о них (время окончания, минимальная ставка, описание продукта).
	- Покупатель делает ставку на аукционе.
	- Покупатель может обращаться к строке поиска вбивая тег или название продукта, для поиска подходящего ему аукциона.
	- После завершения аукциона победитель (покупатель поставивший наивысшую ставку) обязуется оплатить продукт, после - продавец обязуется его доставить.

3. Определите объекты, о которых будут храниться данные.

	- Информация об объекте
	- Информация о покупателе для предложения ему
	- Информация о продавце, его надёжности
	- Информация о текущем аукционе - тут слот для объекта и итоговые обязательства
	- Аукцион внутри:
	- Ставка - это ставит пользователь
	- Время окончания (переносим пользователя в победителя) - задаёт продавец
	- Описание объекта - продавец
	- Покупатель, Продавец - система задаёт
    
    --Покупатель
--Продавец  
--Объект  
-Ставка  
(Объект + ставка возможно внутри аукциона)  
--Аукцион

-Тот кто обязан оплатить
-Тот кто обязан доставить  
(возможно тоже внутри Аукциона)
    
    
4. Определите связи между объектами для хранения данных.  
	Информация о... (и куда она нужна)
    
    - О покупателе - для поиска и предложенийю  
	- О продавце - для пользователя и окна предложенных аукционовю  
	- О объекте - для окна аукциона.  
	- О аукционе - в слот для продавца нужна дата о продавце, в слот для покупателя нужен слот покупателяю

	Таким образом выигравшая ставка покупатель переносится в слот обязанностей оплаты  
	А продавец переносится в слот обязанностей по доставке после оплаты  


5. Нарисуйте схему объектной модели (используя любые обозначения, которые вам удобны).  
	![schema](./schema.png)
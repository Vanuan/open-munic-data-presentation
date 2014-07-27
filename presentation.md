# Open Municipal Data
## Открытые данные местных советов

---

## Проблемы, которые существуют сегодня

* UX сайтов местных органов
* Неполнота данных (не все данные доступны)
* Данные не машиночитаемы

---


## UX сайтов местных органов

![UX](/open-munic-data-presentation/ux.png)

Сложная навигация

---

## UX сайтов местных органов

![UX2](/open-munic-data-presentation/ux2.png)

Скучно!

---

## Неполнота данных

![Data absent](/open-munic-data-presentation/data_absent.png)

Нарушение законодательства

---

## Данные не машиночитаемы

	<p>
	<span style="font-family: arial,helvetica,sans-serif; font-size: 10pt;">
	<a href="/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1292%3A2012-03-05-09-27-48&Itemid=266&lang=uk">
	<span face="arial, helvetica, sans-serif">
	<span size="2">
		Антощук Іван Васильович
	</span></span>
	</a>
	</span></p>

Монополия => отсутствие конкуренции => плохие сайты

---

### Кто уже пытался решать эти проблемы

* хороший UX Липецкого облсовета (РФ) http://www.oblsovet.ru/
* простой сервис для сельсоветов http://rada.info 
* многочисленные CMS. См. список облсоветов https://github.com/Maidan-hackaton/state-administration/blob/master/data/municipal_websites.csv
* Open legislative data http://popoloproject.com/, http://sunlightfoundation.com/

---

## Как мой проект решает проблему

* Scraping -> open data
* Open data -> анализ и представление

---

## Как мой проект решает проблему (technical)

* Scripts -> csv (Python)
* csv -> JSON API (Ruby on Rails)
* JSON API -> appearance (JS/HTML/CSS)

---

## Как мой проект решает проблему (csv)

	Задорожнюк Василь Миколайович,1966-05-01,,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1330%3A2012-03-06-09-27-09&Itemid=266&lang=uk
	Тіндюк Микола Андрійович,,http://oblrada.odessa.gov.ua/images/stories/kerivn/Tindyk.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&id=1415%3A2012-03-12-08-49-20&catid=105&Itemid=266&lang=uk
	Антощук Іван Васильович,1953-09-15,http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Antoschyk/1.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1292%3A2012-03-05-09-27-48&Itemid=266&lang=uk
	Локайчук Валерій Федорович,1957-05-06,http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Lokaichyk/1.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1354%3A2012-03-07-09-19-23&Itemid=266&lang=uk
	Єрьоменко Ігор Володимирович,1966-06-22,http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Eremenko/1.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1326%3A2012-03-06-09-19-41&Itemid=266&lang=uk
	Візнюк Олександр Дмитрович,,,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1282%3A2012-03-05-12-47-12&Itemid=266&lang=uk
	Затула Василь Савович,,,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1332%3A2012-03-06-09-29-15&Itemid=266&lang=uk
	Борняков Олександр Сергійович,1982-03-01,http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Borniakov/1.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&id=1277%3A2012-03-12-08-10-17&catid=105&Itemid=266&lang=uk
	Швець Василь Сергійович,1951-04-14,http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Shvets/1.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1410%3A2012-03-07-10-52-39&Itemid=266&lang=uk
	Смірнов Ігор Володимирович,1968-09-03,http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Smirnov/1.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&id=1164%3A2012-03-06-00-35-12&catid=105&Itemid=266&lang=uk
	Станков Владислав Миколайович,,http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Stankov/1.jpg,http://oblrada.odessa.gov.ua/index.php?option=com_content&view=article&catid=114%3A2012-03-12-08-21-50&id=1391%3A2012-03-07-10-18-11&Itemid=266&lang=uk


---

## Как мой проект решает проблему (json)


	   {
	      "name":"Задорожнюк Василь Миколайович",
	      "date_of_birth":"1966-05-01",
	      "place_of_birth":null,
	      "image":"http://oblrada.odessa.gov.ua/images/stories/DEPUTAT/Zadoroznyuk/1.jpg",
	      "age":48,
	      "related_documents":0,
	      "media_stories":0
	   }


---

## Как мой проект решает проблему (html)

![Demo](/open-munic-data-presentation/demo.png)

---

## Аудитория

* Программисты могут использовать open data для альтернативного анализа/представления
* Граждане получают выбор удобного представления публичной информации

---

## Команда

* Ivan Yani https://github.com/Vanuan/
* Open Source https://github.com/Maidan-hackaton


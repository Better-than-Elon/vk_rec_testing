# Выберите метрику и обоснуйте этот выбор.
Очевидно, что для рекомендаций выбираем метрики serendipity😆(Нет). <br /> Для поставленной задачи решил использовать метрику релевантности, учитывающую ранжирование, потому что пользователям лучше рекомендовать сначала самые подходящие айтэмы, но при этом лучше не выбирать какие-то сложные метрики. Поэтому я выбрал встроенный в LightFM precision@k.
# Придумайте и обоснуйте способ разбиения данных на обучение и валидацию.
Если мы хотим спрогнозировать, как интересы пользователей изменятся во времени, то выбираем тестовые данные после обучающих по времени (но для данной задачи выбрал рандомный сплит 70/30)
# Обратите внимание на сходимость обучения и настройку важных гиперпараметров моделей.
Для настройки гиперпараметров  для LightFM использовал opuna. А в качестве Loss функции выбрал ранжирующий лосс - WARP(Умно семплирует негативные примеры)
# Выберите лучшую модель
В моём коде первая модель учитывает рейтинги и жанры. Вторая учитывает только рэйтинги. Получилось, что первая работает немного лучше, что логично.
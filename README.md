import random

print('добро пожаловать в магический шар, напиши свой вопрос:')

b = ['Бесспорно','Мне кажется - да','Пока неясно, попробуй снова','Даже не думай',
'Предрешено	Вероятнее всего	Спроси позже','Мой ответ - нет','Никаких сомнений','Хорошие перспективы','Лучше не рассказывать',
'По моим данным - нет','Определённо да','Знаки говорят - да','Сейчас нельзя предсказать','Перспективы не очень хорошие',
'Можешь быть уверен в этом','Да','Сконцентрируйся и спроси опять','Весьма сомнительно']

def union(b):
    while True:
        n = input()
        if '?' not in n:
            print('это не вопрос')
            union(b)
        else:
            pass
        random_num = random.choice(b)
        print(random_num)
        if n == 'Мне кажется - да' or n == 'Вероятнее всего' or n == 'Хорошие перспективы':
            print('я не определился,попробуй снова')
            union(b)
        print('чтобы выйти из игры напиши все если нет,то напиши любой символ')
        a = input()
        if a == 'все':
            break
        else:
            print('напиши вопрос')

union(b)

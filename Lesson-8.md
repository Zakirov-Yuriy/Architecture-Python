Spaghetti Code // Спагетти-код
Я конечно не уверен но это единственное что я нашел.

    def __call__(cls, *args, **kwargs):
        global name
        if args:
            name = args[0]
        if kwargs:
            name = kwargs['name']

        if name in cls.__instance:
            return cls.__instance[name]
        else:
            cls.__instance[name] = super().__call__(*args, **kwargs)
            return cls.__instance[name]


Вся моя работа это: Методологические антипаттерны, Reinventing the wheel // Изобретение велосипеда.

В Файле main.py у меня Jumble // Путаница
Его можно структурировать. Разделить на 3 или 2 файла.
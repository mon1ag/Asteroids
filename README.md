# Asteroids
 
Приветствую. 

В папке Build лежит играбельная версия.

Код лежит в папке Scripts.

Код игры разбит на части, каждая контролирует свой объект: SpawnerScript, AsteroidScript, PlayerScript, BulletScript, AlienScript.

SpawnerScript управляет появлением корабля игрока, летающих тарелок, астеройдов. Высчитывает для астеройдов повороты через вращение к определенной точке на краю обзора камеры, контролирует выход игрока за границы экрана, "общается" с UI.
Таймеры спавна новых астеройдов сделаны через float для удобного контроля над ними.
Каждое появление летающей тарелки уменьшает задержку до появления следующего астеройда.
За каждое попадание по врагу дается 5 очков, не стал усложнять этот момент.
Все "общение" с UI специально вынес в один скрипт.

AsteroidScript управляет движением, поворотом и стадией астеройда. Всего стадий три: 3 - большой и медленный, делится на стадии 2 и 1; 2 - средняя скорость и размер, делится на две 1 стадии; 1 - быстрый и маленький.
Направление движения и разлета при деленнии контролируется поворотами. Уничтожаются по таймеру.

PlayerScript управляет движением и стрельбой игрока, отлавливает его смерти.

BulletScript управляет движением снаряда и отлавливает попадания, уничтожается по таймеру.

AlienScript управляет движением летающей тарелки.

Параметры игры и обькетов вынесены в инспектор.
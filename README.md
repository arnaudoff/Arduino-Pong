# Проект по “Компютърни архитектури”

### Съдържание

#### I. Увод

- Тема
- История
- Описание
- Цел и възможности
  - Цел
  - Възможности
- Задание
- Екип

#### II. Проучване

- Цел на проучването
- Проекти

#### III. Принцип на работа

- Съставни компоненти
- Външна конструкция
  - Поглед отстрани
  - Поглед отгоре
- Принципна блок схема

#### IV. Имплементация

- Визуализация
  - Описание
  - Схема
- Отчитането на входните данни
  - Описание
  - Схема
   - Схема на свързване на TCRT5000 към Arduino.
   - Схема на отчитане на входни данни
- Управление на визуализацията на изходните данни
  - Описание
  - Схема
   - Схема на свързване на MAX7219 към Arduino.
   - Схема на каскадно свързване на MAX7219 към Arduino.
- Визуализацията на изходните данни
  - Описание
  - Схема
   - Схема на KF 1088AB-2
- Равносметка
 
#### V. Бъдещо развитие

- Уголемяване на игралното поле
- Поддръжка на множество играчи
- Поддръжка на персистентна система за следене на резултатите на играчите.

#### VI. Приложение

---

### I. Увод

#### 1. Тема
Играта "Pong".

#### 2. История
Играта *Pong*, позната още като *(PONG)*, е една от най-старите аркадни игри и първата спортна аркадна видеоигра. Това е игра от тип тенис, характеризираща се с проста 2D графика. Докато други аркадни видеоигри като *Computer Space* са дошли преди нея, *Pong* е една от първите видео игри, достигнали преобладаваща популярност. Завършена на 29.11.1972 от Алън Алкорн като упражнение, тя бива издадена от [Aтари](https://www.atari.com/) и бързо достига голям успех. Тя е първата търговски успешна аркадна видео игра, което подпомага развитието на индустрията, заедно с първата домашна конзола *Magnavox Odyssey*.

#### 3. Описание

Този проект има за цел да пресъздаде не безизвестната игра Pong във формата на мултиплейър игра (за двама), която се играе на поле, съставено от матрица от светлинни диоди. Имплементацията на играта ще следва правилата на традиционния Pong. 
В полето се пуска топче със зададена скорост и посока. Когато топчето премине границата на полето при един от играчите, 
другият получава една точка. Целта на играчите е с “пръчките” си да отблъснат топчето и да го запратят към полето на противника, така че той да не съумее да го спаси. След получаване на определен брой точки, единият играч бива обявен за победител.

Всеки от играчите ще може с ръка да управлява “пръчката” си. Управлението ще става със сензори, които отчитат позицията на ръката спрямо полето. Самите “пръчки” ще се изобразяват със светодиоди. Със светодиоди също така ще се показва и топчето. През Ардуино ще управляваме логиката за отблъскването на топчето от “пръчките”, преместването им, преместването на топчето, логиката за точките и победата.

Точките на играчите ще се показват отделно и ще се обновяват динамично.

#### 4. Цел и възможности

##### 4.1. Цел
- Да се реализира multiplayer вариант на играта "Pong" за двама играча.
- Всеки да може да управлява “пръчката” си с ръка. 
- Да се запазват и показват точките на двамата играчи.

##### 4.2. Възможности

Изработването на описаната версия на тази игра ще предостави възможност за:
- запознаване със начина, по който създаването на игри се е превърнало в индустрия
- как са се появили различните жанрове и разновидности
- по-обстойно запознаване с embedded програмирането
- изработване и изчисляване на електрически схеми
- практическо приложение и затвърждаване на знанията, придобити преди и по време на курса по "Компютърни архитектури"

#### 5. Задание
- Изграждане на полето за игра като LED матрица.
- Отчитане на движение на ръката на играч.
- Преместване на “пръчката” спрямо положението на ръката.
- Показване на топчето върху полето.
- Отчитане на победа/загуба, когато топчето премине границата на полето в половината на някой играч.
- Отчитане и броене на резултата на играчите.
- Показване на резултатите на играчите.
- Излъчване на победител в играта.

#### 6. Екип

- Ивайло Стефанов Арнаудов 11Б, №13
- Николай Василев Карагьозов 11Б, №22
- Радостин Ангелов Ангелов 11Б, №27
- Христо Езекиев 11А, №28

### II. Проучване

#### 1. Цел на проучването

Да се разучат други проекти със същата тема и да се сравнят реализациите им спрямо нашата.

#### 2. Проекти

##### 1. [Линк](bit.ly/1Z8lbM9)

- В този проект движението на пръчките в играта е реализирано чрез 2 потенциометъра, свързани към Ардуино. С движене на потенциометъра пръчката, която му съответства, се измества нагоре и надолу. 
- Имплементацията на играта е реализирана на езика C. 
- Визуализацията става през телевизор, който е свързан към Ардуино устройството.

###### Сравнение

- При нашия проект движението на пръчките става чрез движение на ръката. То се засича от сензори, който определят позицията на пръчката.
- Имплементацията на играта също е реализирана на езикът C. 
- Визуализацията става през няколко 16 8x8 LED матрици, които показват позицията на топчето.

##### 2. [Линк](http://bit.ly/1VMVel9)

- В този проект движението на пръчките в играта е реализирано чрез 2 потенциометъра, свързани към Ардуино. С движене на потенциометъра пръчката, която му съответства, се измества нагоре и надолу. 
- Имплементацията на играта е реализирана на езика C. 
- Визуализацията става през точно един TFT дисплей.

###### Сравнение

- При нашия проект движението на пръчките става чрез движение на ръката. То се засича от сензори, който определят позицията на пръчката.
- Имплементацията на играта също е реализирана на езикът C. 
- Визуализацията става през 9 бр. 8x8 LED матрици, които показват позицията на топчето.

##### 3. [Линк](https://sites.google.com/site/alastairparker/arduinopong)
- В този проект отново визуализирането на игралното поле става върху монитор.
- Имплементацията на играта е реализирана на езика C.
- Синхронизацията на нишките за двамата играча става чрез изключване на прекъсването за време на atmega168.

###### Сравнение

- Разликата между това, да гледаме играта на монитор и на собствено игрално поле, е че при игралното поле играча по-добре навлиза в атмосферата на играта.

##### 4. [Линк](http://www.itopen.it/arduino-pong-with-8x8-led-matrix-and-max7219)
- При този проект, както се вижда целта е била подобна на нашата, като са използвани същите елементи - 8x8 LED матрица, с MAX7219 за управляване на конкретните светодиоди. 
- Проектът използва една матрица, което означава малко игрално поле, неудобно за един играч, камо ли за двама. 
- Имплементацията съдържа бъгове, поради които на моменти топчето изглежда че заема два диода. Играта се играе от един играч.

###### Сравнение

- Ние ползваме няколко 8x8 LED матрици, които ще позволят по-удобно следене на играта и управление на “пръчките”. 
- По-голямото място ще позволи да играят 2-ма играча.

##### 5. [Линк](https://github.com/giacomocerquone/Arduino-Pong-TVout)

- Отново имплементация на играта, използваща телевизор за визуализация.
- Тази имплементация позволява игра от двама човека, като синхронизирането на нишките става чрез два цикъла с изчакване.

###### Сравнение

- Визуализацията става през 9 бр. 8x8 LED матрици, които показват позицията на топчето.

##### 6. [Линк](http://madeformakers.org/2016/01/26/creating-a-pc-2-player-pong-game-controller-with-arduino-and-processing)

- Проекта реализира играта pong на компютър, като използва Arduino за контрол над двамата играча. 
- Ардуиното се свързва към компютър през /dev/ttyACM. 
- Контрола над играчите става с помощта на два потенциометъра.

###### Сравнение

- При нашия проект движението на пръчките става чрез движение на ръката. То се засича от сензори, който определят позицията на пръчката.
- Отново се вижда разликата в начините на визуализация на играта. Нашата игра не използва дисплея на компютър, а 8x8 LED матрици за рисуване на двете “пръчки” и топчето. Това значително увеличава трудността на проекта от гледна точка на създаване на електронната схема, както и имплементиране на логиката на играта - рисуване на отделните елементи и съответно синхронизация на действията на двамата играча и движението на топчето.

##### 7. [Линк](http://blog.theincredibleholk.org/blog/2014/06/16/arduino-pong)

- Създадена е singleplayer игра като е използван дисплей за визуаилзация.
- При достигане на топчето до някоя от стените на полето съответни на краищата на полетата на играчите, играта не свършва, а топчето се отблъсква и променя посоката си.

###### Сравнение

- Нашата игра използва 8x8 LED матрици за визуализация.
- Когато топчето се удари в някоя от стените - краища на полетата на играчите, срещуположният играч печели. Това съответно увеличава резултата на печелившия играч. 
- Резултатите на двамата играчи са видими и се обновяват динамично.

##### 8. [Линк](http://lucidtronix.com/tutorials/7)

- Играта използва LCD дисплей за визуализация и два джойстика (COM-09032) за управление на “пръчките”.
- След преминаване на топчето през част от екрана, то оставя плътна следа.

###### Сравнение

- Ние използваме сензори за засичане на движенито на ръцете на играчите, с които се управляват двете “пръчки”. Това допринася за по добра атмосфера на играта.
- Екрана на играта се изчиства след преминаване на топчето през него, за по-лесно наблюдение на играта.

##### 9. [Линк](http://electronics.divinechildhighschool.org/Home/electronics-spring-2012-1/arduino-pong)

- Играта следва традиционната игра от 70-те. Играта се визуализира върху телевизор като за целта се използва arduino-tvout библиотеката.

###### Сравнение

- За визуализация на играта използваме 8x8 LED матрици и MAX7219 за по-лесно управление на отделните светодиоди.

### III. Принцип на работа

#### 1. Съставни компоненти

Проекта се състои от няколко компонента:
- Arduino Mega 2560
- хардуерен бутон за рестарт на играта
- една голяма 3x3 матрица, която представлява 9 бр. 8x8 LED матрици
- два светодиода, съответно по един за играч, индикиращи победителя в конкретната сесия
- 8 бр. сензори, разделени по 4 за всеки от играчите
- корпус на цялата конструкция

#### 2. Външна конструкция

##### 2.1. Поглед отстрани
![Поглед отстрани](http://puu.sh/oSvgE/52c298e0c5.jpg)

##### 2.2. Поглед отгоре
![Поглед отгоре](http://puu.sh/oSvqX/016bafd72a.jpg)

#### 3. Принципна блок схема
![Блок схема](https://i.imgur.com/Q7NrO1h.png)

### IV. Имплементация

#### 1. Визуализация

##### 1.1. Описание

##### 1.2. Схема

![Ел. схема](http://i.imgur.com/jSB87Ca.png)

#### 2. Отчитането на входните данни

##### 2.1 Описание

Следенето на движението на ръцете на хората се извършва с помощта на TCRT5000 - отразяващ оптичен сензор, с транзисторен изход.
 
![Ел. схема](https://i.imgur.com/lDTRN1E.png)

Сензорът се състои от две части - светодиод излъчващ инфрачервена светлина и фототранзистор. Светодиода излъчва светлинен сигнал, който се променя при отражение от обект и се поема от фототранзистора, тази промяна после предизвиква промяна в елкетрическия сигнал идващ от фототранзистора. Светодиода излъчва светлинен сигнал, с дължина на вълната 950nm, а максималното разстояние на отчитане е 2.5М. Основните характеристики на TCRT5000 могат да се видят в приложение №1.
Ние използваме сигналът, идващ от фототранзистора, за да определим позицията на ръката на играча и с това да изчертаем пръчката на играча на екрана. По принцип този тип сензори се използват като се чете аналоговият сигнал, който те подават. С него може по-точно да се определи далечината на обекта и така по-добре да се определи къде точно се намира спрямо дължината на полето, като се вземат предвид стойностите от всички сензори от съответната страна на полето. Начина на изрисуване на пръчката на играча обаче - върху матрици с големина 8x8, не изисква такава точност и позволява използването на по-прост начин - с цифрови стойности. Ниска стойност(0) от сензорите означава, че пред тях има предмет, който отразява светлината - ръката на играча, а висока, че цялата светлина се поема от транзистора, което означава че пред светодиода няма нищо, което да отрази светлината.

##### 2.2. Схема

###### 2.2.1. Схема на свързване на TCRT5000 към ардуино.

![Ел. схема](https://i.imgur.com/Rf6CGS7.png)

###### 2.2.2. Схема на свързване на всичките сензори

![Ел. схема](https://s32.postimg.org/mwvnz6qfp/tcrt_circuit.png)

###### 2.2.3. Схема на отчитане на входни данни

#### 3. Управление на визуализацията на изходните данни

##### 3.1 Описание

За управление на LED матриците използваме сериите интегрални схеми MAX72XX и по-конкретно MAX7219, макар че MAX7221 също би била рационален избор. Основното предимство на IC при управлението на матриците е че се използват само три изхода на Arduino за управление на до 64 светодиодa, което става през SPI slave interface. При управлението на повече от една LED матрица използваме т.нар cascaded принцип.

##### 3.2 Схема

###### 3.2.1 Схема на свързване на MAX7219 към Arduino.

![Ел. схема](http://playground.arduino.cc/uploads/Main/MAX72XX_SPI.jpg)

###### 3.2.2 Схема на каскадно свързване на MAX7219 към Arduino.

![Ел. схема](https://i.imgur.com/OdwgMYw.png)

#### 4. Визуализацията на изходните данни

##### 4.1 Описание

За визуализация на игровата логика използваме девет 8x8 матрици KF 1088AB-2 със стандартна схема общ анод.

##### 4.2 Схема

###### 4.2.1 Схема на KF 1088AB-2

![Ел. схема](https://dcw9y8se13llu.cloudfront.net/avatars/Deeder_M.jpg)

#### 5. Код

```C
#include <LedControl.h>

typedef struct vec_t {
  int x;
  int y;
};

typedef enum {
  NONE,
  LEFT,
  RIGHT
} ROUND_WINNER;

LedControl lc = LedControl(51, 53, 52, 1);

const int MATRIX_SIZE = 8;
const int MATRIX_SQUARE_SIDE = 1; // Describes how many by how many matrices we have.
const int NUMBER_OF_SENSORS = 8;
const int PADDLE_LENGTH = 2;

int tcrt_sensors[NUMBER_OF_SENSORS] { 0 };
const int tcrt_pins[NUMBER_OF_SENSORS] = { 30, 32, 34, 36, 31, 33, 35, 37 };

vec_t left_paddle_pos { 0, 0 };
vec_t right_paddle_pos { MATRIX_SIZE - 1, 0 };

vec_t ball_pos { 2, MATRIX_SIZE / 2 };
vec_t ball_direction { 1, 1 };

ROUND_WINNER check_victory(ROUND_WINNER winner);
void reset_if_won();

void clear_at(vec_t pos);
void clear_screen();

void display_at(vec_t pos);
void display_paddle(vec_t pos);

void handle_ball_collisions();
void update_ball_position();

void read_sensors();

void setup() {
  Serial.begin(9600);
  lc.shutdown(0,false);
  lc.setIntensity(0,8);
  lc.clearDisplay(0);
  int i;
  for(i = 0; i < NUMBER_OF_SENSORS; i++) {
    pinMode(tcrt_pins[i], INPUT_PULLUP);
    digitalWrite(tcrt_pins[i], HIGH);
  }
}

void loop() {
  clear_screen();
  
  read_sensors();
  
  handle_ball_collisions();
  update_ball_position();
  
  display_paddle(left_paddle_pos);
  display_paddle(right_paddle_pos);
  display_at(ball_pos);

  delay(500);
}

void read_sensors() {
  int i;
  for (i = 0; i < NUMBER_OF_SENSORS; i++) {
    tcrt_sensors[i] = digitalRead(tcrt_pins[i]);
  }
};

void update_ball_position() {
  ball_pos.x += ball_direction.x;
  ball_pos.y += ball_direction.y;
}

void modify_direction_if_nessesary() {
  if (ball_pos.x == 0) {
    ball_direction.x = 1;
  }
  
  if (ball_pos.x == MATRIX_SQUARE_SIDE * MATRIX_SIZE - 1) {
    ball_direction.x = -1;
  }

  if (ball_pos.y == 0) {
    ball_direction.y = 1;
  }
  
  if (ball_pos.y == MATRIX_SQUARE_SIDE * MATRIX_SIZE - 1) {
    ball_direction.y = -1;
  }
}

void reset_if_won(ROUND_WINNER winner) {
  if (winner != NONE) {
    if (winner = LEFT)
      Serial.println("Left won");
    else
      Serial.println("Right won");

    ball_pos.x = 2;
    ball_pos.y = MATRIX_SIZE / 2;
  }
}

ROUND_WINNER check_victory() {
  if (ball_pos.x == 0 && ball_direction.x == -1)
    return RIGHT;
  if (ball_pos.x == MATRIX_SIZE - 1 && ball_direction.x == 1)
    return LEFT;
  return NONE;
}

void handle_ball_collisions() {
  ROUND_WINNER winner = check_victory();
  reset_if_won(winner);
  modify_direction_if_nessesary();
  modify_direction_if_nessesary();
}

void clear_paddle(vec_t paddle_pos) {
  int i;
  for (i = 0; i < PADDLE_LENGTH; i++) {
    vec_t current { paddle_pos.x, paddle_pos.y + i };
    clear_at(current);
  }
}
void clear_screen() {
 clear_paddle(left_paddle_pos);
 clear_paddle(right_paddle_pos);
 clear_at(ball_pos);
}

void clear_at(vec_t pos) {
  lc.setLed(0, pos.x, pos.y, false);
}

void display_paddle(vec_t pos) {
 int i;
 for (i = 0; i < PADDLE_LENGTH; i++) {
  vec_t current { pos.x, pos.y + i };
  display_at(current);
 }
}

void display_at(vec_t pos) {
  lc.setLed(0, pos.x, pos.y, true);
}
```

#### 6. Равносметка

- 1 x Arduino Mega 2560 - 82лв.
- 8 x TCRT-5000 - 2 лв.
- 9 x MAX7219 - 15лв.
- 9 x KF 1088AB-2 - 12лв.
- 2 x ПП 160mmx100mm - 12лв.
- 80-90 x male джъмпера - 10лв.
- 10-20 x резистори ~ 2лв.
- 10-20 x кондензатори ~ 2лв.

Общо: ~140лв.

### V. Бъдещо развитие

#### 1. Уголемяване на игралното поле

За момента схемата се състои от 3x3 LED матрици и 4x2 TCRT 5000 IR сензори. Бъдещо развитие може да бъде осъществено като се увеличи броят на матриците и респективно броят на сензорите. Пример 5х5 конфигурация на матриците придружена от 8 сензора разпределени на равно разстояние един от друг от всяка страна, на която има играч.

#### 2. Поддръжка на множество играчи

В момента игралното поле поддържа 2 играча максимум. На матричното поле, от страната на всеки играч, се визуализира пръчка, която може да се движи чрез сензори, поставени откъм съответната страна. Останалите непокрити от играчи страни се считат за стени и топката отскача, когато се удари в тях. Игралното поле има възможността да поддържа 4 играча. Това може да се реализира като от всяка страна на игралното поле стои играч, които има предопределен брой сензори, с които контролира пръчката си. В тази имплементация няма да има стени в играта и топчето ще може да променя посоката си единствено ако се удари в пръчка. Възможен недостатък на този подход представлява затруднението да се броят резултатите на играчите. Конвенционалният подход, които се използва при 2 играча увеличава резултата на човекът, който е увладял топката и я е изпратил зад противниковата пръчка с 1. При 4 играча това е непрактично, тъй като човек изпусне топката, има трима други играча, който трябва да бъдат наградени. Възможни решения на този проблем са:
- Увеличаване на резултата на последния играч, докоснал топката.
  - Недостатък на този подход е, че има възможността последният докоснал топката да не е заслужил резултатът си.
- Увеличаване на резултата на всички играчи, с изключение на загубилия.
  - Недостатък тук е, че играчи, който не са участвали в рунда може да получават точки "безплатно".
- Намаляне на резултата на загубилия.
  - Този подход е най-удачен, тъй като е възможно да се играе в стил "последният оцелял". Всички играчи започват с определен брой точки и с всяко пропускане на топката съответният играч губи точка. Победител е единственият, който има над 0 точки на полето. Местата на загубилите играчи се заместват със стени.

#### 3. Поддръжка на персистентна система за следене на резултатите на играчите.

След края на всеки рунд се обявява победител. Възможност за развитие на сегашната игра e система, която следи всички резултати играчите. Това може да бъде реализирано чрез wi-fi модул, свързан към Arduino-то, който изпраща данни на отдалечен сървър, който от своя страна ги запазва в база данни. Данните от сървъра могат да бъдат визуализирани на уеб страница като резултатите са разделени на два типа: такива на левия и десния играч.

### VI. Приложение

#### 1. 83760 datasheet, http://www.vishay.com/, 2012 
#### 2. MAX7219 datasheet, https://datasheets.maximintegrated.com/en/ds/MAX7219-MAX7221.pdf

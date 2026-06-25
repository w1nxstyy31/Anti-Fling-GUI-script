# Silent

```lua
loadstring(game:HttpGet('https://raw.githubusercontent.com/w1nxstyy31/Anti-Fling-GUI-script/refs/heads/main/Silent.lua'))()
```






# Anti-Fling-GUI-script
Всем привет! Для тех, кто из России - пролистайте ниже.

# ENG

Tired of getting flung by skids? Then this script is exactly what you need.

Hey guys! To be honest, this is my very first script, but I put a ton of effort into making it as robust and polished as possible. It comes in two different versions:
  
  Light Version: Allows you to move around freely with decent, reliable protection.
  Silent Version: Disables movement but offers maximum protection, automatically teleporting you back to your activation point every 5 seconds.

**So, which one should you choose?**

  It honestly depends on your needs. If you need to navigate the map, go with the Light version. In practice, it’s more than enough to protect you from kids running popular public fling scripts.The Silent version is geared towards
  enthusiasts who need absolute, impenetrable defense for things like auto-farming. Performance-wise, the Light version currently lags quite a bit behind the Silent one in terms of raw protection, but that’s only for now. I am fully
  committed to improving and updating this script in the future, aiming to achieve the highest level of security possible for the Light version.

**How do they work?**

  Light Version: Creates a detection zone that continuously monitors the velocity and angular velocity changes of all parts inside nearby player models. If any player comes within 30 studs of you, the script flags them for 
  inspection. If it detects rapid, unnatural spikes in their velocity or rotational speed, it forces their client-side Velocity (linear speed) and RotVelocity (angular rotational speed) to zero. Additionally, the script disables 
  collisions (CanCollide = false) for the flagged player on your client, applies a complete noclip effect to your own character (LocalPlayer), and forces your humanoid into the NoPhysics state.
  
  Silent Version: Unlike the Light version, which relies on basic collision toggles and reactive velocity resets, the Silent version operates on the advanced PreSimulation event. This phase is processed before the Roblox physics 
  engine calculates any physical contacts or impacts. Every single frame, the script forces your character's AssemblyLinearVelocity and AssemblyAngularVelocity to absolute zero. This guarantees that even if an exploiter physically 
  touches you, the engine cannot transfer any kinetic energy or rotational torque to your character.Furthermore, the detection radius is expanded to 45 studs. The moment an exploiter crosses this boundary, the script applies a 
  targeted, multi-layered countermeasure:It disables their character's collisions (CanCollide = false) strictly on your client, making them completely intangible to you.It completely wipes all variations of their velocity data 
  (Velocity, RotVelocity, and AssemblyLinearVelocity), instantly neutralizing the kinetic energy of their fling script before they can even get close.It overwrites their physical properties with zeroPhysicalProperties (zero mass and
  zero friction). To your client, the exploiter literally becomes as weightless as a feather, making it physically impossible for them to push anything.On top of all this, it runs your client through the core safety checks utilized 
  in the Light version for a definitive layer of redundancy.

**Why should I trust you?**
 
  Believing what is written above is entirely up to you. However, I have uploaded a video showcase featuring extensive tests against various fling scripts on my YouTube channel. 
  You are more than welcome to go and see the results for yourself.

**Which fling scripts does it counter?**

  Personally, I have tested it against Infinite Yield (fling, walkfling, invisfling), FE Fling GUI by Blue_boy2816, and Ultimate Fling GUI by Kilasik. Not a single one managed to fling the Silent version. Draw your own conclusions.

**Why do I need this script if I can just turn on Noclip?**

  I actually tested this too using Infinite Yield. For reasons unknown to me, standard Noclip doesn't always work, and when it does, it doesn't last long. This exact issue is what motivated me to create this script in the first place.

**What avatar types does it support? R6 or R15?**

  It protects you everywhere, completely regardless of your character type.

# RUS

Устал терпеть флинг от skid'ов? Тогда этот скрипт для тебя.
Всем привет! Честно говоря этот скрипт мой первый, но я конкретно постарался сделать его максимально хорошим. У него есть 2 версии:

1 - Light (есть возможность ходить, средняя защита)
2 - Silent (отсутствует возможность ходить, максимальная защита, телепорт каждые 5 секунд на место от куда вы нажали кнопку)

**Так какую же мне выбрать?**
  На самом деле зависит от тебя. Если нужно передвигаться по карте можно пользоваться Light версией, она на практике способна защитить тебя от детей которые используют популярные Fling-скрипты.
  а Silence для интузиастов, которым для чего то нужна максимальная защита(автофарм там всякий), в деле Light очень сильно проигрывает Silence по защите, но это пока. Я в будущем обязательно буду улучшать и 
  обновлять данный скрипт пытаясь достичь максимальной безопасности которая возможна в Light.

**В чем их функционал?**
  
  Light - Cоздает область, в которой проверяет скорость и скорость изменения Rotation всех обьектов состоящих в моделе игроков по близости, в случае если к вам подойдет любой человек меньше чем на 30 студов - это вызовет подозрения 
  в его сторону, а затем скрипт проверит его, и если обнаружит резкие изменения в его скорости и в скорости изменения Rotation всех обьектов состоящих в его моделе, то принудительно обнулит его параметры Velocity(линейная скорость) и 
  RotVelocity(угловая скорость вращения), еще скрипт отключит коллизию у врага(на клиенте) и полностью коллизию у каждой части LocalPlayer(по сути noclip), потом скрипт принудительно заставляет вашего персонажа находиться в системном 
  состоянии NoPhysics.

  Silence - В отличие от версии Light, которая просто выключала коллизию вам и обнуляла скорость обьектов читера, версия Silent работает на продвинутом событии PreSimulation (это этап, который обрабатывается ДО того, как физический 
  движок Roblox успеет просчитать соприкосновение объектов). Каждый кадр скрипт обнуляет параметры AssemblyLinearVelocity и AssemblyAngularVelocity у вашего персонажа. Это гарантирует, что если читер заденет вас, движок Roblox 
  физически не сможет передать вам его крутящий момент. Скрипт сканирует карту теперь в увеличенном радиусе — 45 единиц (в Light было всего 30). Как только читер пересекает эту черту, скрипт точечно воздействует на него:
  Выключает ему коллизию (CanCollide) только на вашем клиенте.
  Полностью обнуляет все виды его скоростей (Velocity, RotVelocity, AssemblyLinearVelocity), мгновенно гася всю кинетическую энергию его Fling-скрипта еще до того, как он подлетит к вам.
  Назначает его деталям свойства zeroPhysicalProperties (нулевой вес и нулевое трение). Для вашего клиента этот читер буквально становится невесомым пухом, который не способен ничего толкнуть.
  И прогоняет ваш клиент по параметрам с версии Light.

**С чего это я должен тебе верить?**

  Верить в выше перечисленные слова - твое решение. Но я выложил видеобзор с тестами разных Fling-скриптов на свой YouTube канал. Сам лично можешь взять и проверить.

**А какие Fling-скрипты он контрит?**

  Лично я тестировал его на Inf Yield(fling, walkfling, invisfling), на Fe Fling Gui от Blue_boy2816 и на Ultimate Fling Gui от Kilasik. Ни у одного не получилось флингануть Silence версию. Выводы делайте сами.

**Зачем мне этот скрипт, если я могу просто включить NoClip?**

  Это я тоже проверял, использовал Inf Yield и по не известной мне причине NoClip контрит не всегда и не долго. Меня это как раз таки и подтолкнуло на создание данного скрипта.

**Какие модели игрока он поддерживает? R6/R15?**
  Он защищает тебя везде, вне зависимости от типа персонажа.

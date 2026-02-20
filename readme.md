# Лабораторная работа №1

<div align="center">

**МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ**  
**ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ**  
**«САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»**

<br>
<br>

Институт естественных наук и техносферной безопасности  
Кафедра информатики  
Пахомов Владимир Романович

<br>
<br>
<br>
<br>

Лабораторная работа №1  
**«Android empty app»**  
01.03.02 Прикладная математика и информатика  
3 Курс

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<div align="right">
Научный руководитель<br>
Соболев Евгений Игоревич
</div>

<br>
<br>
<br>

г. Южно-Сахалинск  
2026 г.

</div>

---  

## Цель Работы

Изучить структуру Android-проекта в среде разработки Android Studio, освоить процесс создания и модификации пользовательского интерфейса, научиться запускать приложение на эмуляторе, а также закрепить навыки работы с файлами ресурсов.

## Скриншоты
![](Снимок%20экрана%202026-02-20%20193153.png)  
<br>
![](Снимок%20экрана%202026-02-20%20193402.png)

## Fisting
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/greeting"
        android:textColor="#E93838"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/greetings"
        android:textColor="#E93838"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.546" />

</androidx.constraintlayout.widget.ConstraintLayout>
  ```

## Ответы на контрольные вопросы

**1. Какие ключевые элементы составляют структуру Android-проекта?**  
В среде Android Studio проект обычно состоит из следующих основных частей:

- **`Manifests`** — хранит конфигурационный файл `AndroidManifest.xml`, который содержит мета-данные о приложении.
- **`Java` / `Kotlin`** — директория с исходным кодом, где располагаются активности, классы и бизнес-логика.
- **`Res` (Resources)** — хранилище ресурсов приложения: макеты интерфейсов (`layout`), графические элементы (`drawable`), текстовые строки (`values/strings.xml`), стили и цвета.
- **`Gradle Scripts`** — скрипты сборки (в частности, `build.gradle`), отвечающие за подключение зависимостей и настройку компиляции.

**2. Каково назначение файла AndroidManifest.xml?**  
Файл `AndroidManifest.xml` выступает в роли основного описателя приложения для системы Android. В нем регистрируются ключевые параметры: название программы, иконка, перечень всех активностей (экранов), а также права доступа (permissions), необходимые для работы функционала.

**3. В чем разница между minSdkVersion и targetSdkVersion?**  
- **`minSdkVersion`** — определяет минимальную версию ОС Android, которая поддерживается приложением. На устройствах с версией ниже этой установить приложение не удастся.
- **`targetSdkVersion`** — указывает версию Android, для которой приложение было специально разработано и протестировано. Это помогает системе понимать, какие механизмы совместимости применять при запуске на новых версиях ОС.

**4. Что представляет собой AVD и зачем он нужен?**  
**AVD** (Android Virtual Device) — это настройка эмулятора, имитирующего реальное устройство Android. Он позволяет разработчикам запускать, отлаживать и тестировать приложения на ПК, не используя физические смартфоны или планшеты.

**5. Каким образом можно поменять текст приложения, не трогая код активности?**  
Для этого следует использовать систему ресурсов. Текст хранится в отдельном файле **`strings.xml`** (путь `res/values/`). В разметке (`layout`) или коде программы текст вызывается через ссылку на ресурс (например, `@string/имя_строки`). Благодаря этому, чтобы изменить надпись, достаточно внести правки только в файл ресурсов, не затрагивая программный код.

## Вывод

По итогам выполнения работы были освоены принципы организации проекта в Android Studio, изучено назначение ключевых файлов: манифеста (`AndroidManifest.xml`), ресурсов (`res`) и скриптов сборки (Gradle). Также был настроен и запущен эмулятор (AVD) для отладки.

Практическая часть включала редактирование пользовательского интерфейса: модификацию файла разметки `activity_main.xml`. В макет был добавлен дополнительный элемент `TextView`, скорректированы параметры шрифта и цветовой схемы. Все текстовые данные были вынесены в ресурсный файл `strings.xml`, что обеспечивает удобство локализации и редактирования контента в будущем.

Финальное тестирование показало, что приложение корректно запускается на виртуальном устройстве, что свидетельствует об отсутствии ошибок в коде и верной конфигурации проекта.


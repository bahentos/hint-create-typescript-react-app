# Шпаргалка-create react-app typescript
---
## Используемые технологии

> [React](https://ru.reactjs.org/docs/getting-started.html), 
[Redux Toolkit](https://redux-toolkit.js.org/introduction/getting-started),
[TypeScript](https://www.typescriptlang.org/docs/handbook/typescript-from-scratch.html),
[Ant Design](https://ant.design/components/overview/),

## **React и TypeScript**
### Установка
```
yarn create react-app my-app --template typescript
```
### Настройки
Могут понадобиться настройки для TypeScript. Для этого нужно модифицировать файл конфигурации `tsconfig.json`
```
{

  "compilerOptions": {

    "target": "es2016", // Укажите целевую версию ECMAScript

    "lib": [

      "dom",

      "dom.iterable",

      "esnext"

    ], // Список файлов библиотеки для включения в компиляцию

    "allowJs": true, // Разрешить компиляцию файлов JavaScript

    "skipLibCheck": true, // Пропустить проверку типов всех файлов объявлений

    "esModuleInterop": true, // Отключает импорт пространства имен (импорт * как fs из "fs") и включает импорт в стиле CJS / AMD / UMD (импорт fs из "fs")

    "allowSyntheticDefaultImports": true, // Разрешить импорт по умолчанию из модулей без экспорта по умолчанию

    "strict": true, // Включить все параметры строгой проверки типов

    "forceConsistentCasingInFileNames": true, // Запрещаем ссылки с несогласованным регистром на один и тот же файл.

    "module": "esnext", // Указываем генерацию кода модуля

    "moduleResolution": "node", // Разрешить модули в стиле Node.js

    "isolatedModules": true, // Безоговорочно генерировать импорт для неразрешенных файлов

    "resolveJsonModule": true, // Включить модули, импортированные с расширением .json

    "noEmit": true, // Не выводить вывод (то есть не компилировать код, а только выполнять проверку типа)

    "jsx": "preservees2016", // Поддержка JSX в файлах .tsx

    "sourceMap": true, // Создание соответствующего файла .map

    "declaration": true, // Создаем соответствующий файл .d.ts

    "noUnusedLocals": true, // Сообщать об ошибках на неиспользуемых локальных объектах

    "noUnusedParameters": true, // Сообщаем об ошибках неиспользуемых параметров

    "incremental": true, // Включить инкрементную компиляцию путем чтения/записи информации из предыдущих компиляций в файл на диске

    "noFallthroughCasesInSwitch": true // Сообщать об ошибках для случаев падения в инструкции switch

  },

  "include": [

    "src/**/*" // *** Файлы TypeScript должны ввести проверку ***

  ],

  "exclude": ["node_modules", "build"] //  *** Файлы, которые не нужно вводить, проверять ***

}
```
> Обратите внимание на пункт `"allowJs": true` - очень рекомендуется если вам нужно типизировать готовый, старый проект. Позволяет использовать `js` и `jsx` файлы при компиляции typescript

## **Redux Toolkit**
### Установка
```
yarn add redux
yarn add @reduxjs/toolkit
```
### Настройки

Добавить импорт над строчкой src/App.css в файле App.tsx
```
import 'antd/dist/antd.css'
```

## **Ant Design**
### Установка
```
yarn add antd
```
### Настройки

Добавить импорт над строчкой src/App.css в файле App.tsx
```
import 'antd/dist/antd.css'
```
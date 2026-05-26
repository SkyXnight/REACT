| Раздел      | Тема                   | Что нужно понимать             | Пример                     |
| ----------- | ---------------------- | ------------------------------ | -------------------------- |
| Основы      | JSX                    | HTML внутри JS                 | `<h1>Hello</h1>`           |
| Основы      | Components             | UI разбивается на части        | `function Button()`        |
| Основы      | Props                  | Передача данных parent → child | `<User name="Alex" />`     |
| Основы      | State                  | Данные компонента              | `useState()`               |
| Основы      | Rerender               | Компонент вызывается заново    | `setCount()`               |
| Основы      | Event Handling         | Работа с событиями             | `onClick`                  |
| Основы      | Controlled Inputs      | React управляет input          | `value + onChange`         |
| Основы      | Conditional Rendering  | Условный UI                    | `isLoading ?`              |
| Основы      | List Rendering         | Вывод массива                  | `todos.map()`              |
| Основы      | key                    | Уникальный ключ списка         | `key={todo.id}`            |
| Основы      | Forms                  | Работа с form                  | `onSubmit`                 |
| Основы      | preventDefault         | Отмена reload формы            | `e.preventDefault()`       |
| Основы      | CRUD                   | Create Read Update Delete      | Todo App                   |
| Основы      | Immutability           | Нельзя мутировать state        | `{...todo}`                |
| Основы      | Spread Operator        | Копирование объектов           | `{...user}`                |
| Hooks       | useState               | State + rerender               | `useState(0)`              |
| Hooks       | useEffect              | Side effects                   | fetch/localStorage         |
| Hooks       | Dependency Array       | Когда effect запускается       | `[]`, `[todos]`            |
| Hooks       | Cleanup                | Очистка effect                 | `clearInterval()`          |
| Hooks       | useRef                 | DOM refs / хранение значений   | `inputRef.current.focus()` |
| Hooks       | useMemo                | Кэш значений                   | `filteredTodos`            |
| Hooks       | useCallback            | Кэш функций                    | `handleClick`              |
| Hooks       | Custom Hooks           | Своя логика                    | `useTodos()`               |
| Архитектура | Parent → Child         | Props flow                     | `<TodoItem />`             |
| Архитектура | Child → Parent         | Callback functions             | `onDelete(id)`             |
| Архитектура | Lifting State Up       | Общий state выше               | App хранит todos           |
| Архитектура | Reusable Components    | Переиспользуемые компоненты    | `<Button />`               |
| Архитектура | Component Splitting    | Разделение UI                  | TodoList/TodoItem          |
| Архитектура | Single Source of Truth | Один главный state             | useTodos                   |
| Оптимизация | React.memo             | Защита от rerender             | `memo(TodoItem)`           |
| Оптимизация | useMemo                | Кэш вычислений                 | `filter()`                 |
| Оптимизация | useCallback            | Стабильные функции             | `deleteTodo`               |
| Оптимизация | Rerender Flow          | Почему компонент обновился     | state/props                |
| TypeScript  | Props Typing           | Типизация props                | `type Props = {}`          |
| TypeScript  | useState Typing        | Тип state                      | `useState<string>()`       |
| TypeScript  | Array Typing           | Типизация массивов             | `Todo[]`                   |
| TypeScript  | Function Typing        | Типизация функций              | `(id:number)=>void`        |
| TypeScript  | Event Typing           | Типизация событий              | `React.ChangeEvent`        |
| TypeScript  | Optional Props         | Необязательные props           | `title?: string`           |
| TypeScript  | Union Types            | Несколько типов                | `string \| null`           |
| TypeScript  | Generics Basics        | Обобщённые типы                | `<T>`                      |
| Async/API   | async/await            | Асинхронность                  | `await fetch()`            |
| Async/API   | Promise                | “Данные будут позже”           | `fetch()`                  |
| Async/API   | fetch API              | HTTP запросы                   | `fetch(url)`               |
| Async/API   | JSON                   | parse/stringify                | `JSON.parse()`             |
| Async/API   | try/catch              | Обработка ошибок               | API errors                 |
| Async/API   | Loading State          | Состояние загрузки             | `isLoading`                |
| Async/API   | Error State            | Состояние ошибки               | `isError`                  |
| Async/API   | REST API Basics        | GET POST PUT DELETE            | todos API                  |
| Local Data  | localStorage           | Хранилище браузера             | `setItem()`                |
| Local Data  | Synchronization        | sync state + storage           | useEffect                  |
| Local Data  | Persisted State        | Данные после refresh           | todos                      |
| Структура   | Folder Structure       | Архитектура проекта            | components/hooks           |
| Структура   | Separation of Concerns | UI отдельно от logic           | useTodos                   |
| Структура   | components/            | UI компоненты                  | TodoItem                   |
| Структура   | hooks/                 | Логика                         | useTodos                   |
| Структура   | types/                 | TypeScript типы                | todo.ts                    |
| Структура   | utils/                 | Helper functions               | formatDate                 |
| Практика    | Todo App               | CRUD + state                   | Todo                       |
| Практика    | Weather App            | API + loading                  | Weather API                |
| Практика    | Notes App              | localStorage                   | Notes                      |
| Практика    | Search App             | filtering                      | search/filter              |
| Практика    | Dashboard              | composition                    | cards/charts               |

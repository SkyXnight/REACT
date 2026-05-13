| Тема                     | Что это                                       | Как работает                                       | Пример                                   |
| ------------------------ | --------------------------------------------- | -------------------------------------------------- | ---------------------------------------- |
| JSX                      | HTML внутри JavaScript                        | React читает JSX и превращает его в настоящий HTML | `return <h1>Hello</h1>`                  |
| `{}` в JSX               | JavaScript внутри JSX                         | React вычисляет выражение и вставляет результат    | `<h1>{name}</h1>`                        |
| Fragment `<> </>`        | Позволяет вернуть несколько элементов без div | React группирует элементы без лишнего HTML         | `<> <h1/> <p/> </>`                      |
| className                | Атрибут классов в React                       | React превращает `className` в обычный `class`     | `<div className="box">`                  |
| Компонент                | Функция возвращающая JSX                      | React вызывает функцию и рендерит JSX              | `function Button() { return <button/> }` |
| Использование компонента | Вставка компонента в JSX                      | React вызывает компонент как функцию               | `<Button />`                             |
| Props                    | Данные для компонента                         | React передает props объект в компонент            | `<User name="Dima" />`                   |
| Destructuring props      | Достает свойства из props                     | Создаются отдельные переменные                     | `function User({ name })`                |
| children                 | Всё внутри компонента                         | React передает внутренний JSX в `children`         | `<Card>Hello</Card>`                     |
| useState                 | Хук для state                                 | React хранит значение между рендерами              | `const [count, setCount] = useState(0)`  |
| State                    | Данные компонента                             | При изменении React делает rerender                | `setCount(5)`                            |
| Setter функция           | Обновляет state                               | React получает новое значение и обновляет UI       | `setCount(count + 1)`                    |
| Rerender                 | Повторный вызов компонента                    | React заново вызывает функцию компонента           | `App()`                                  |
| State объект             | Хранение объекта в state                      | React хранит объект как состояние                  | `useState({ name: "Dima" })`             |
| Spread оператор          | Копирование объекта/массива                   | Создается новый объект/массив                      | `{ ...user, age: 20 }`                   |
| State массив             | Массив внутри state                           | React хранит массив между рендерами                | `useState([])`                           |
| Добавление в массив      | Создание нового массива                       | Spread копирует старые элементы                    | `[...todos, newTodo]`                    |
| onClick                  | Событие клика                                 | React вызывает функцию при нажатии                 | `<button onClick={handleClick}>`         |
| onChange                 | Изменение input                               | React получает новое значение input                | `<input onChange={...} />`               |
| Event object             | Объект события                                | React передает данные о событии                    | `(e) => console.log(e)`                  |
| e.target.value           | Значение input                                | React получает введенный текст                     | `e.target.value`                         |
| onSubmit                 | Отправка формы                                | React вызывает функцию submit                      | `<form onSubmit={...}>`                  |
| preventDefault           | Отмена reload страницы                        | Браузер не перезагружает страницу                  | `e.preventDefault()`                     |
| Controlled Input         | Input связанный со state                      | Value всегда берется из state                      | `value={text}`                           |
| Conditional Rendering    | Условный рендер                               | React показывает JSX по условию                    | `{isAdmin && <Admin />}`                 |
| Ternary operator         | if/else внутри JSX                            | React выбирает один из двух JSX                    | `{isLogged ? <Home /> : <Login />}`      |
| map()                    | Создание списка JSX                           | React проходит по массиву и рендерит элементы      | `todos.map(todo => <li />)`              |
| key                      | Уникальный id элемента                        | React понимает какой элемент изменился             | `key={todo.id}`                          |
| useEffect                | Хук side effects                              | React запускает код после рендера                  | `useEffect(() => {}, [])`                |
| Dependencies             | Зависимости useEffect                         | React следит за изменением значений                | `[count]`                                |
| Cleanup                  | Очистка effect                                | React вызывает cleanup перед удалением             | `return () => {}`                        |
| fetch                    | HTTP запрос                                   | Браузер отправляет запрос на сервер                | `await fetch(url)`                       |
| async                    | Асинхронная функция                           | Позволяет использовать await                       | `async function getData()`               |
| await                    | Ожидание Promise                              | Код ждет завершения Promise                        | `await fetch()`                          |
| res.json()               | Парсинг JSON                                  | JSON превращается в JS объект                      | `await res.json()`                       |
| Loading state            | Состояние загрузки                            | React показывает loader во время запроса           | `setLoading(true)`                       |
| Error state              | Состояние ошибки                              | React показывает ошибку пользователю               | `setError(err)`                          |
| useRef                   | Ссылка на DOM                                 | React хранит объект между рендерами                | `const ref = useRef()`                   |
| ref.current              | DOM элемент                                   | current содержит HTML элемент                      | `ref.current.focus()`                    |
| Context API              | Глобальный state                              | React передает данные через дерево                 | `createContext()`                        |
| Provider                 | Передает context                              | Дочерние компоненты получают value                 | `<Theme.Provider>`                       |
| useContext               | Получение context                             | React берет value из Provider                      | `useContext(ThemeContext)`               |
| React Router             | Роутинг React                                 | React меняет страницы без reload                   | `<Route path="/" />`                     |
| Routes                   | Контейнер роутов                              | React ищет подходящий route                        | `<Routes>`                               |
| Route                    | Описание страницы                             | React показывает component по URL                  | `<Route path="/about" />`                |
| Link                     | Переход между страницами                      | React меняет URL без reload                        | `<Link to="/about" />`                   |
| useNavigate              | Навигация кодом                               | React меняет страницу через JS                     | `navigate("/profile")`                   |
| useMemo                  | Кэширование вычислений                        | React не пересчитывает значение                    | `useMemo(() => total)`                   |
| useCallback              | Кэширование функций                           | React сохраняет функцию между рендерами            | `useCallback(() => {})`                  |
| React.memo               | Оптимизация компонента                        | React пропускает лишний rerender                   | `React.memo(Button)`                     |
| Custom Hook              | Свой hook                                     | Переиспользование логики                           | `function useFetch()`                    |
| TypeScript Props         | Типизация props                               | TS проверяет типы props                            | `type Props = {}`                        |
| TypeScript Events        | Типизация событий                             | TS знает тип event                                 | `React.ChangeEvent<HTMLInputElement>`    |
| Local Storage            | Хранение данных браузера                      | Данные сохраняются после reload                    | `localStorage.setItem()`                 |
| Redux Toolkit            | Глобальный state manager                      | State хранится в store                             | `createSlice()`                          |
| Store                    | Хранилище state                               | Все данные лежат в одном месте                     | `configureStore()`                       |
| Reducer                  | Изменение state                               | Reducer возвращает новый state                     | `reducers: {}`                           |
| TanStack Query           | Работа с серверным state                      | React кэширует запросы                             | `useQuery()`                             |
| useQuery                 | GET запросы                                   | Query получает и кэширует данные                   | `useQuery({})`                           |
| useMutation              | POST/PUT/DELETE                               | Mutation изменяет данные                           | `useMutation()`                          |
| Next.js                  | Framework для React                           | Добавляет SSR и routing                            | `app/page.tsx`                           |
| SSR                      | Server Side Rendering                         | HTML создается на сервере                          | Быстрая загрузка                         |
| CSR                      | Client Side Rendering                         | React рендерит всё в браузере                      | Обычный React                            |
| Lazy Loading             | Загрузка по частям                            | React загружает код только когда нужно             | `React.lazy()`                           |
| Suspense                 | Loader для lazy                               | Показывает fallback во время загрузки              | `<Suspense fallback={...}>`              |
| Error Boundary           | Ловит ошибки React                            | React показывает fallback UI                       | `<ErrorBoundary>`                        |
| Tailwind CSS             | Utility-first CSS                             | Стили пишутся классами                             | `className="flex"`                       |
| CRUD                     | Работа с данными                              | Create Read Update Delete                          | Todo App                                 |
| Authentication           | Авторизация                                   | Login/logout пользователя                          | JWT/Auth                                 |

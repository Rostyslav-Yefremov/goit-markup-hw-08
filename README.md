ДЗ

Заметки:

<!-- 1. Если на макете нет заголовка секции, но он там напрашивается - каким образом
   его добавить?

2. Фото, картинки в jpg, а лого-иконки в svg
3. ctrl+/ - закомментирует
4. Focus и Active можно дать только на интерактивные елементы - кнопки, ссылки,
   формы, а Hover на любой, Visited только на ссылку.
5. Для цвета в основном используйте Хексы, РГБ только для прозрачности
6. Порядо важен - побеждает тот селектор, которой ниже (если одинаковая
   специфичность)
7. Лучшая разметка для стилей - классы по имени родителя и ребенка через -
8. Последовательность написания стилей в селекторе: 1 - размер, 2 - оформление
   цвета, 3 - оформление текста, 4 - декоративный элемент
9. .list { list-style:none } - стили по умолчанию обнулять лучше так, в
   дальнейшем глобальные стили не приветствуются -->

Вопрос по контейнерам

маргинам и падингам

цвет, размеры ,ховеры

Вопросы:

1. Тулзы - гид
2. Классы - допкассы, наследование

- задать 320 в тулзах
- Убираем флексы
- Контейнеру задать 100 процентов ширину
- 100% лишке и списку
  @media screen and ( min-width: 480px)
  max-width: 480px

.container {
margin-left: auto;
margin-right: auto;
padding-left: 15px;
padding-right: 15px;
width: 100%;
@media screen and (min-width: 480px) {
max-width: 480px;
}
@media screen and (min-width: 768px) {
max-width: 768px;
}
@media screen and (min-width: 1200px) {
max-width: 1200px;
}
}

(() => {
const refs = {
openMenuBtn: document.querySelector('.menu-open'),
closeMenuBtn: document.querySelector('.menu-close'),
menu: document.querySelector('.mobile-nav'),
};

refs.openMenuBtn.addEventListener('click', toggleMenu);
refs.closeMenuBtn.addEventListener('click', toggleMenu);

function toggleMenu() {
refs.menu.classList.toggle('is-hidden');
}
})();

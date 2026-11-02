# Редактирование, проверки и публикация

## Быстрые ссылки
- [Опубликованный сайт](https://ekatmoz88-alt.github.io/fintech-docs-demo/)
- [Репозиторий](https://github.com/ekatmoz88-alt/fintech-docs-demo)
- [Запуски Actions](https://github.com/ekatmoz88-alt/fintech-docs-demo/actions)
- [Pages workflow](../.github/workflows/pages.yml)

## Проверка перед публикацией
- [ ] Текстовый сценарий и диаграмма процесса согласованы.
- [ ] Роли и разрешения операторов описаны однозначно.
- [ ] Правила PII-маскирования и доступа понятны.
- [ ] Audit log не предлагает сохранять секреты или полные чувствительные данные.
- [ ] Ссылки и ресурсы сайта проверены.
- [ ] Pages workflow завершился успешно.
- [ ] [Опубликованный сайт](https://ekatmoz88-alt.github.io/fintech-docs-demo/) открывается.

## Диагностика
Откройте последний запуск [GitHub Actions](https://github.com/ekatmoz88-alt/fintech-docs-demo/actions), найдите первый упавший step и проверьте Pages permissions и artifact. Публикация настроена на изменения в site/** и workflow; сверяйте фактические фильтры с YAML.

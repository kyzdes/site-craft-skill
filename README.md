# site-craft

Скилл для Claude Code и Codex: как сделать стильный сайт или лендинг. Речь не о конкретном дизайне, а о порядке решений, который дал budka.app.

## Порядок

1. Метафора: где продукт живёт физически. Это становится сценой страницы.
2. Палитра и шрифты из продукта: у каждого цвета записанная роль, акцент один.
3. Референсы с Mobbin по блокам, из каждого взята одна вещь (нужен `mobbin-pool`).
4. Мудборд: что берём у других, три живых направления в HTML, рекомендация. Направление выбирает человек.
5. Каждый блок — работающая мини-демонстрация, примеры сквозные.
6. Короткий честный текст (вычитка — `clarity`).
7. Запреты: свечения, пилюли, карточки-сетки, анимации на месте (проверка — `impeccable`).
8. Детали: ничего не прыгает, reduced motion, фокус, og-картинка шрифтами сайта.
9. Работа итерациями: одна правка за раз, git перед смелым шагом, проверка на 1440 и 375.

Всё — в [`skills/site-craft/SKILL.md`](skills/site-craft/SKILL.md).

## Установка

Claude Code:

```text
/plugin marketplace add kyzdes/claude-skills
/plugin install site-craft@claude-skills
```

Codex (скиллы пользователя лежат в `~/.agents/skills`):

```bash
git clone --depth 1 https://github.com/kyzdes/site-craft-skill /tmp/site-craft-skill
mkdir -p ~/.agents/skills && rm -rf ~/.agents/skills/site-craft
cp -R /tmp/site-craft-skill/skills/site-craft ~/.agents/skills/
rm -rf /tmp/site-craft-skill
```

Затем новый чат в Codex. Позвать скилл: «сделай сайт…» или `$site-craft`.

Референсы с Mobbin скилл берёт через MCP-сервер `mobbin`. Без него попросит скриншоты или ссылки.

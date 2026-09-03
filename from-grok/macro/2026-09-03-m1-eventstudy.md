# M1-REACT — event-study NFP → BTCUSDT 1h (K-0)

Статус: Knowledge Candidate. Не Foundation. Не вход. Не слот WR≥60% доски паттернов.
Дата заморозки: 2026-09-03
Слой: `from-grok/2026-09-03-macro-scenario.md`
Данные: тот же K-0, что P1 (BTCUSDT 1h Binance Vision). Консенсус/факт NFP — публичный архив (Investing/FXStreet calendar history или BLS CES + сторонний survey archive с URL). Look-ahead: только значения, известные на дату t.

## Зачем

Измерить, есть ли устойчивая реакция BTC на сюрприз занятости США. Карту стороны не угадывать. Если устойчивого знака нет — честно написать и оставить слой как предупреждение окна, не как вход.

## if/then прогона (ЗАМОРОЖЕН)

```
Вселенная: пятничные NFP 08:30 America/New_York в покрытии K-0.
Бар события t = 1h-бар, внутри которого 12:30 UTC (летнее 13:30 UTC — брать фактический offset даты).
consensus, actual — с URL; нет пары → строка выкидывается, не подставлять.
band = 20_000 занятых.
bucket = BEAT если actual-consensus > band; MISS если < −band; иначе INLINE.

r_1h  = close[t+1] / close[t-1] − 1
r_4h  = close[t+4] / close[t-1] − 1
r_1d  = close[t+24]/ close[t-1] − 1   (если бар есть)
impulse = 1 если |r_1h| ≥ 0.003 иначе 0

Сдать по bucket: n, mean r_1h, mean r_4h, доля impulse.
Отдельно: n всего, сколько строк выкинуто без consensus.
```

n<20 в bucket → `INSUFFICIENT_SAMPLE` для этого bucket, не средний по всем.

Не live. Пороги P1 не трогать. Git Тестер не пишет — сдаёт штабу.

## Что не делать

Не подкручивать band после цифр. Не клеить с зигзагом. Не обещать «NFP down → BTC up». Не FRED dump в git.

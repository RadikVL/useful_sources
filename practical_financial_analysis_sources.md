# Прикладные источники для статистического и матанализа финансовых инструментов

Если нужен именно `прикладной` стек для статистического/матанализа `stocks / FX / crypto`, то я бы рекомендовал вот это.

## Самое полезное на старте

- [Analysis of Financial Time Series](https://dev.store.wiley.com/en-in/Analysis%2Bof%2BFinancial%2BTime%2BSeries%2C%2B3rd%2BEdition-p-9780470644560) — Ruey S. Tsay  
  Что дает: `returns`, `volatility clustering`, `ARIMA`, `GARCH`, multivariate time series, применение к реальным финансовым рядам.  
  Зачем читать: это одна из самых прикладных книг именно под анализ финансовых инструментов, а не “абстрактную статистику”.  
  Уровень: `средний -> продвинутый`

- [Quantitative Trading](https://nl.mathworks.com/academia/books/quantitative-trading-chan.html) — Ernest P. Chan  
  Что дает: построение простых systematic strategies, `backtest`, `mean reversion`, `momentum`, инфраструктура квант-ресерча.  
  Зачем читать: очень хороший вход в практический quant mindset.  
  Уровень: `база -> средний`

- [Algorithmic Trading: Winning Strategies and Their Rationale](https://la.mathworks.com/academia/books/algorithmic-trading-chan.html) — Ernest P. Chan  
  Что дает: более структурный разбор `mean reversion`, `momentum`, `risk management`, логики альфы и проверки гипотез.  
  Зачем читать: уже ближе к реальному research workflow, чем обычные “книги про трейдинг”.  
  Уровень: `средний`

## Если хочешь делать research нормально, а не подгонять BTC

- [Advances in Financial Machine Learning](https://dev.store.wiley.com/en-us/Advances%2Bin%2BFinancial%2BMachine%2BLearning-p-00000140) — Marcos Lopez de Prado  
  Что дает: `labeling`, `purged CV`, sampling, feature importance, борьба с leakage и false positives.  
  Зачем читать: полезно, если ты уже используешь `ML`, и хочешь меньше заниматься самообманом в бэктестах.  
  Уровень: `продвинутый`

- [The Probability of Backtest Overfitting](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2326253) — Bailey et al.  
  Что дает: понимание, почему “нашел рабочую стратегию” часто означает “перебрал слишком много вариантов”.  
  Зачем читать: must-read для любого, кто тестирует гипотезы на исторических данных.  
  Уровень: `продвинутый`

- [Deflating the Sharpe Ratio](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2460551) — Bailey, Lopez de Prado  
  Что дает: как корректировать оценку Sharpe с учетом multiple testing и selection bias.  
  Зачем читать: после этого намного осторожнее смотришь на результаты бэктеста.  
  Уровень: `продвинутый`

## Для intraday / FX / crypto это особенно важно

- [Trading and Exchanges: Market Microstructure for Practitioners](https://academic.oup.com/book/52292) — Larry Harris  
  Что дает: `order book`, спред, ликвидность, типы участников, исполнение ордеров, рыночная механика.  
  Зачем читать: без этого анализ FX/crypto/stocks часто остается анализом свечек, а не рынка.  
  Уровень: `средний`

- [Algorithmic and High-Frequency Trading](https://www.cambridge.org/us/search?query=Algorithmic+and+High-Frequency+Trading) — Cartea, Jaimungal, Penalva  
  Что дает: более формальный взгляд на `execution`, order book dynamics, intraday modeling, optimal execution.  
  Зачем читать: особенно полезно, если смотришь на short-horizon alpha, market making, execution-sensitive стратегии.  
  Уровень: `продвинутый`

## Практические инструменты, чтобы не читать только книги

- [statsmodels Time Series / User Guide](https://www.statsmodels.org/stable/user-guide.html)  
  Что дает: `ARIMA`, `VAR`, `state space`, regressions, hypothesis tests.  
  Зачем читать: это прямой рабочий инструмент для ресерча по ценам, спредам, факторным моделям.  
  Уровень: `база -> средний`

- [arch package documentation](https://bashtage.github.io/arch/)  
  Что дает: `GARCH`, volatility models, unit root tests, cointegration, bootstrap.  
  Зачем читать: очень полезно именно для финансовых рядов, особенно когда анализируешь volatility и mean reversion.  
  Уровень: `средний`

## Если совсем коротко, что брать тебе

1. `Tsay`
2. `Chan: Quantitative Trading`
3. `Chan: Algorithmic Trading`
4. `Harris`
5. `statsmodels` + `arch`
6. Потом уже `Lopez de Prado`

## Как это разложить по рынкам

- `Акции`: `Tsay`, `Chan`, `Lopez de Prado`, `statsmodels`
- `FX`: `Tsay`, `Harris`, `Cartea`, `arch`
- `Crypto`: `Harris`, `Cartea`, `Chan`, `Lopez de Prado`
- `Для всех трех`: `Tsay`, `statsmodels`, `arch`, papers по overfitting`

## Что можно сделать следующим шагом

Если хочешь, следующим сообщением можно собрать узкий practical roadmap именно под твой профиль:

1. `для statistical arbitrage`
2. `для ML по кросс-секции акций`
3. `для intraday/crypto/market microstructure`
4. `для FX time-series research`

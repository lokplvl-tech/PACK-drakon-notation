# Ontology: Нотация ДРАКОН

> Domain ontology per SPF.SPEC.002.

---

## 1. Entity Types

| Code | Type | FPF/SPF Concept | Definition | ≠ (what it is NOT) | Source |
|------|------|-----------------|------------|---------------------|--------|
| `M` | Method | U.Method | Способ перевести табличный метод в ДРАКОН-схему | ≠ сценарий, ≠ инструмент | SPF (base) |
| `WP` | Work Product | U.Work + U.Episteme | Готовая схема, прошедшая проверки; при необходимости - код | ≠ описание метода | SPF (base) |
| `FM` | Failure Mode | — (SPF-specific) | Именованное в первоисточнике нарушение правил языка | ≠ дефект конкретной схемы без названного правила | SPF (base) |
| `D` | Distinction | A.7 Strict Distinction | Пара терминов языка, которые путают | ≠ факт, ≠ определение | SPF (base) |
| `R` | Role | U.RoleAssignment | Функциональное место - построение и проверка схемы | ≠ человек, ≠ должность | SPF (base) |
| `SOTA` | SoTA Annotation | — (SPF-specific) | Тезис из первоисточника Паронджанова | ≠ пересказ по памяти | SPF (base) |
| `MAP` | Map | U.Episteme | Карта Pack | ≠ содержание | SPF (base) |

---

## 2. Domain Glossary

| Term (RU) | Term (EN) | Definition | Parent Concept (SPF) | Related entity |
|-----------|-----------|-----------|---------------------|----------------|
| Икона | icon | Графоэлемент языка - Заголовок, Действие, Вопрос и др. | U.System | DRK.M.001 |
| Шампур-блок | skewer | Часть схемы с одним входом сверху и выходом снизу на одной вертикали | U.System | DRK.D.004 |
| Примитив | primitive | Простой алгоритм без веток | U.System | DRK.D.001 |
| Силуэт | silhouette | Сложный алгоритм, разбитый на именованные ветки | U.System | DRK.D.001 |
| Главный маршрут | main route | Путь к наибольшему успеху - крайняя левая вертикаль | U.Characteristic | DRK.D.002 |
| Сиамские близнецы | siamese twins | Запрещённое слияние двух веток в одной точке | — (FM) | DRK.FM.001 |
| Три царских вопроса | three royal questions | Как называется задача? Из скольких частей состоит? Как называется каждая часть? | U.Method | DRK.M.001 |
| Диосцена | dioscene | Двумерная оптическая сцена для панорамного восприятия схемы | U.Characteristic | 01A-bounded-context |

---

## 3. Relationships Between Types

| Subject | Relationship | Object | Example |
|---------|-------------|--------|---------|
| Method | produces → | Work Product | DRK.M.001 → готовая схема |
| Failure Mode | violates ← | Method (позиция потока) | DRK.FM.001 ← DRK.M.001 поз. 6 |
| Distinction | guards → | Method (позиция потока) | DRK.D.003 → DRK.M.001 поз. 8 |

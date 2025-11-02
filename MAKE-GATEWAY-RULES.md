# 🚨 CRITICAL: Make.com Gateway Rules

**Дата:** 2025-11-02  
**Статус:** PRODUCTION - НЕ ТРОГАТЬ!

## ❌ СТРОГО ЗАПРЕЩЕНО

1. **НИКОГДА не изменять Make.com Gateway workflow (WsVlI8ld32XAk5JV)**
   - Он production, стабильный, полностью работает
   - Все HTTP nodes настроены правильно
   - Token и URLs валидные

2. **НИКОГДА не создавать новые Gateway workflows**
   - Один Gateway достаточно
   - Дубликаты создают путаницу

3. **НИКОГДА не трогать токены/URLs в Gateway** без явного запроса Бориса
   - Token: 1093fee2-60e0-4432-8c6c-205c5706cb6c (working)
   - Team: 2552758 (Brain Index)

4. **НИКОГДА не использовать Make.com MCP напрямую**
   - Работа ТОЛЬКО через n8n Gateway
   - Make.com MCP может быть отключен

## ✅ ОБЯЗАТЕЛЬНО

### Работа с Make.com scenarios

**ВСЯ работа ТОЛЬКО через n8n Gateway:**

**Gateway Webhook:**
```
POST https://annoris.app.n8n.cloud/webhook/make-gateway
Content-Type: application/json
```

**Available Actions:**
```json
{"action": "list"}                                    // Список всех scenarios
{"action": "get", "scenarioId": "7908237"}           // Детали scenario
{"action": "run", "scenarioId": "7908237"}           // Запуск scenario
{"action": "start", "scenarioId": "7908237"}         // Активировать scenario
{"action": "stop", "scenarioId": "7908237"}          // Деактивировать scenario
{"action": "status", "scenarioId": "7908237"}        // Статус scenario
{"action": "logs", "scenarioId": "7908237"}          // Логи executions
{"action": "hybrid", "data": {"taskType": "..."}}    // Routing logic
```

**Example через n8n MCP:**
```javascript
n8n-mcp:n8n_trigger_webhook_workflow({
  webhookUrl: "https://annoris.app.n8n.cloud/webhook/make-gateway",
  httpMethod: "POST",
  data: {"action": "list"},
  waitForResponse: true
})
```

### Gateway Architecture

**Workflow ID:** WsVlI8ld32XAk5JV  
**Name:** Make.com Gateway - ACTIVE  
**Status:** Production, протестирован

**Structure:**
1. Gateway Webhook (POST trigger)
2. Validate Input (проверка action)
3. Action Router (8 веток)
4. API Calls:
   - List Scenarios API
   - Get Scenario API
   - Run Scenario API
   - Start Scenario API
   - Stop Scenario API
   - Get Status API
   - Get Logs API
   - Hybrid Processor
5. Process Response (форматирование)
6. Gateway Response (webhook response)

**All HTTP nodes configured with:**
- Correct Make.com API URLs
- Valid token (1093fee2...)
- Proper parameters

## 🎯 Текущие Scenarios

**Scenario 7908237:** "конвертация голосовых"
- Telegram voice → Whisper → Translation → TTS → Telegram
- Team: 2552758
- Status: В процессе настройки

## 📝 История изменений

**2025-11-02:**
- Gateway полностью настроен и работает
- Все 7 HTTP API nodes починены
- Token обновлен на 1093fee2
- Протестирован через Gateway Test Suite
- Все 4 теста прошли успешно

## ⚠️ ЕСЛИ НУЖНО ИЗМЕНИТЬ GATEWAY

**ОБЯЗАТЕЛЬНО:**
1. СПРОСИТЬ Бориса ПЕРВЫМ
2. Объяснить ЗАЧЕМ нужно изменение
3. Получить явное разрешение
4. Делать backup перед изменением
5. Тестировать после изменения

**НЕ ИЗМЕНЯТЬ:**
- URLs в HTTP Request nodes
- Token в Authorization headers
- Структуру connections
- Validation logic
- Response formatting

## 🚀 Quick Reference

**Список scenarios:**
```bash
POST webhook/make-gateway
{"action": "list"}
```

**Детали scenario:**
```bash
POST webhook/make-gateway
{"action": "get", "scenarioId": "7908237"}
```

**Запуск scenario:**
```bash
POST webhook/make-gateway
{"action": "run", "scenarioId": "7908237"}
```

---

**ЗАПОМНИ:** Gateway работает → не трогай его! Вся работа с Make.com через Gateway.

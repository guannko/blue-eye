# n8n MAKE.COM GATEWAY PROTOCOL

**NEVER create new workflows for Make.com tasks!**
**ALWAYS use existing Make.com Gateway system:**

## PRIMARY WORKFLOW: Make.com Gateway - ACTIVE
- **ID:** WsVlI8ld32XAk5JV
- **Webhook:** https://annoris.app.n8n.cloud/webhook/make-gateway
- **Method:** POST with JSON payload

## AVAILABLE ACTIONS:
```json
{
  "action": "list",                    // List all scenarios
  "action": "get",                     // Get scenario details
  "action": "run",                     // Execute scenario
  "action": "start",                   // Activate scenario  
  "action": "stop",                    // Deactivate scenario
  "action": "status",                  // Get scenario status
  "action": "logs",                    // Get execution logs
  "action": "hybrid"                   // Smart routing logic
}
```

## EXAMPLE USAGE:
```json
{
  "action": "run",
  "scenarioId": "7850736", 
  "data": {"test": "value"},
  "responsive": true
}
```

## SUPPORTING WORKFLOWS:
- **Management Dashboard:** n8n ↔ Make.com overview
- **Client Dashboard:** Client-facing automation control

## CRITICAL RULE:
**Use Gateway, don't create new workflows!**

## CLEAN SYSTEM STATUS:
✅ Make.com Gateway - ACTIVE (WsVlI8ld32XAk5JV)
✅ Management Dashboard (03nKXfd8Jw6YmnOx)  
✅ Client Dashboard (GaCNV0SczPxSYBMx)
❌ All other Make.com workflows - DELETED

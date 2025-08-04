# Ecommerce Notification Service

Sends notifications based on events (e.g., AddressUpdated, OrderPlaced).

## Setup
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Configure event subscriptions:
   ```bash
   # Use config/events.yaml for Kafka/RabbitMQ
   ```
3. Run the service:
   ```bash
   uvicorn src.main:app --reload
   ```

## Endpoints
- `POST /notification`: Send a notification (for testing)

## Dependencies
- Event Bus: For subscribing to events

## Entities
- **Notification**: `{event_type: string, customer_id: Guid, message: string}`

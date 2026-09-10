# Chatbot & AI Concierge Engine (Standalone Bun Binary)

A high-speed, self-contained AI Chatbot and E-Commerce Concierge engine compiled as a standalone Linux binary.

- **Zero dependencies required:** No Node.js, Bun, or NPM needed on the host machine.
- **Built-in Security:** Meta Llama Prompt Guard 2 (22m) jailbreak & injection protection.
- **High Speed:** Sub-millisecond startup and low latency inference with Groq LPU.
- **Master Control Plane:** Programmatic tenant provisioning, live telemetry, and hot-reloadable config.

---

## 🚀 How to Run

### 1. Make Binary Executable
```bash
chmod +x concierge-core
```

### 2. Configure Environment Variables
Create `.env` (or pass via terminal):
```env
PORT=8080
GROQ_API_KEY=your_groq_api_key_here
CONTROL_PLANE_SECRET=antigravity-master-control-secret-108
```

### 3. Run Directly
```bash
./concierge-core
```
The server will boot instantly and listen on `http://localhost:8080`.

---

## 📡 Key Endpoints

| Endpoint | Method | Description |
|---|---|---|
| `/health` | `GET` | Upstream health check & memory telemetry |
| `/control/info` | `GET` | Service discovery manifest & OpenAPI schemas |
| `/api/v1/chat` | `POST` | Core chat completion & autonomous tool dispatcher |
| `/api/v1/guard-check` | `POST` | Dedicated Prompt Guard 2 (22m) inspection |
| `/widget.js` | `GET` | 1-Line Drop-in JavaScript chat widget |
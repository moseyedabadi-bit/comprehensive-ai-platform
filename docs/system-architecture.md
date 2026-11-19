# معماری منطقی سامانه

```mermaid
flowchart LR
  U[کاربر یا سامانه سازمانی] --> G[API Gateway]
  G --> A[احراز هویت و سیاست دسترسی]
  A --> O[AI Orchestrator]
  O --> M[Model Serving]
  O --> R[RAG Service]
  R --> V[(Vector Index)]
  R --> D[(منابع داده مجاز)]
  O --> T[Tool Connectors]
  T --> X[سامانه‌های سازمانی با API مجاز]
  O --> L[Audit & Observability]
  M --> L
```

## اجزا
- **API Gateway:** کنترل نرخ، احراز هویت اولیه و مسیریابی
- **Orchestrator:** اعمال سیاست‌ها، فراخوانی مدل و ابزارها
- **Model Serving:** اجرای مدل با کنترل منابع
- **RAG:** بازیابی اسناد مطابق مجوز هر درخواست
- **Tool Connectors:** اتصال محدود و قابل ممیزی به APIها
- **Observability:** متریک، تریس، رویداد امنیتی و مصرف منابع

دیاگرام نمای منطقی است و ادعای نصب یا راه‌اندازی اجزا ندارد.

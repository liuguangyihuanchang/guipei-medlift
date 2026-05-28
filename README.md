# 规培-medlift 🤖✍️

> **MedLift** = Medical + Lift — 把病历重担从规培医生肩上抬走  
> AI-Powered Medical Documentation for Chinese Residency Training Doctors

---

## 🎯 What It Does

**规培-medlift** (MedLift) is a dual-platform AI documentation tool built for **规培医生 (Chinese residency training doctors)** — the backbone of China's hospital system who handle the heaviest paperwork load with the least time.

| Platform | Function |
|----------|----------|
| **Android App** | Record doctor-patient consultations + snap lab photos → AI auto-generates **入院记录** |
| **Android App** | Narrate in-treatment updates → AI generates **病程记录** |
| **Windows Web Tool** | Input patient history + labs + orders + dates → AI generates **病程记录** via browser |

> **规培 = 规范化培训 (Residency Training)** — China's unique graduate medical training system.  
> These doctors rotate through internal medicine, surgery, and subspecialties, writing hundreds of records per rotation. MedLift exists to get them home on time.

---

## 👤 Who's It For

**Chinese residency training doctors (规培医生)** in internal medicine and surgery.

You're cycling through 10+ patients a day. The last thing you need is another 2 hours of typing after shift ends. MedLift handles the paperwork — you handle the medicine.

---

## 📱 Android App — How It Works

```
第1步   下载安装 MedVox 安卓应用
         ↓
第2步   在阿里云百炼或其他 API 提供商注册
         ↓
第3步   打开 App → 设置页面填入：
         ├── API URL（OpenAI 兼容端点）
         ├── API Key
         └── 模型名称（model name）
         ↓
第4步   开始使用
         ├── 🎙️ 问诊录音 → AI 生成入院记录
         ├── 📸 拍摄检验/检查单 → AI 读取并录入
         └── 🎙️ 口述在院情况 → AI 生成病程记录
```

---

## 💻 Windows Tool — How It Works

Open `ai病历通用结构化prompt.html` in any modern browser:

```
第1步   打开 ai病历通用结构化prompt.html（无需安装，双击即用）
         ↓
第2步   输入：
         ├── 病人既往病史
         ├── 在院检验结果
         ├── 在院检查报告
         ├── 在院医嘱
         └── 入院日期 / 手术日期 / 出院日期
         ↓
第3步   点击「生成 Prompt」→ 提交给 AI
         ↓
第4步   AI 在页面直接生成完整病程记录 → 复制粘贴使用
```

Zero installation. Pure HTML. Works offline after first load.

---

## ⚙️ Technical Stack

```
Android App       Kotlin / Jetpack Compose (原生安卓开发)
                  Voice Recording + Camera
                  OpenAI-Compatible API（支持通义千问 / DeepSeek / 任选模型）

Windows Tool      Pure HTML + JavaScript（无需安装）
                  OpenAI-Compatible API 调用
                  任何现代浏览器均可运行

AI Backend        通义千问 Qwen（阿里云百炼）/ OpenAI-Compatible 任选
```

---

## 🔒 Privacy & Safety

- Patient data is sent **only** to your configured API endpoint
- Audio and photos are processed locally, then sent to your AI provider
- **No data is stored on third-party servers**
- All final records must be reviewed and signed off by the responsible physician

> ⚠️ AI-generated records are **assistential** — final clinical documentation remains the physician's responsibility

---

## 🚀 Getting Started

### Android App

```bash
# 1. Download the APK from GitHub Releases
# 2. Install on your Android device
# 3. Register at 阿里云百炼: https://dashscope.console.aliyun.com/
# 4. Get your API Key and OpenAI-compatible URL
# 5. Fill in Settings → API Configuration
# 6. Start documenting
```

### Windows Tool

```bash
# 1. Open ai病历通用结构化prompt.html in any browser
# 2. Fill in patient data and key dates
# 3. Generate → Submit to AI → Copy result
```

---

## 📁 Project Structure

```
规培-medlift/
├── android/                         MedVox Android App source
├── windows/                         Windows HTML tool
│   └── ai病历通用结构化prompt.html
├── docs/                             Documentation
└── README.md                        This file
```

---

## 📄 License

Apache 2.0

---

**Developer**: 张弘弦  
**Started**: 2026-03-18  
**GitHub**: https://github.com/liuguangyihuanchang/guipei-medlift
# 🎯 How to View Metrics on LangSmith Dashboard

## ✅ Setup Complete!

Your app is now fully integrated with LangSmith. Here's how to view the metrics:

---

## 📊 Step 1: Restart Your Streamlit App

**Important:** You need to restart the app for changes to take effect.

1. Stop your current Streamlit app (press `Ctrl+C` in terminal)
2. Restart it:
   ```bash
   streamlit run streamlit_app_standalone.py
   ```

You should see this in the console:
```
✅ LangSmith tracing enabled - View at: https://smith.langchain.com
```

---

## 🌐 Step 2: View Metrics on LangSmith

### A. Go to LangSmith Dashboard

1. Open your browser and go to: **https://smith.langchain.com**
2. Log in with your account
3. You should see your project: **`concept-map-generator`**

### B. Generate a Concept Map

1. In your Streamlit app, enter a description and click "Generate"
2. Wait for it to complete
3. The metrics are automatically sent to LangSmith!

### C. View the Metrics

Go to https://smith.langchain.com and you'll see:

**Dashboard Overview:**
- **Total runs** - How many times you've generated concept maps
- **Success rate** - Percentage of successful generations
- **Latency chart** - How long each generation took
- **Cost tracking** - Estimated API costs

**Click on any run to see:**
- ⏱️ **Total duration** - How long the entire process took
- 🔍 **Trace view** - Step-by-step breakdown:
  - `create_timeline` - Overall pipeline
  - `extract_concepts_from_full_description` - AI extraction step
  - API call duration, parse time, etc.
- 📝 **Inputs** - The description you entered
- 📊 **Outputs** - Number of concepts and relationships extracted
- 🎯 **Metadata** - Word count, target concepts, all timing metrics

---

## 📈 What You'll See:

### Timeline View
Shows all your runs in chronological order with:
- Duration bars (visual comparison)
- Success/failure status
- Timestamp
- Quick metrics

### Detailed Trace View
Click any run to see a hierarchical view:
```
📍 create_timeline (1.52s)
  ├─ 📝 Inputs
  │  ├─ description: "Photosynthesis is..."
  │  ├─ educational_level: "high school"
  │  └─ topic_name: "Photosynthesis"
  │
  ├─ 🔄 extract_concepts_from_full_description (1.45s)
  │  ├─ API call: 1.23s
  │  ├─ Parse: 0.01s
  │  └─ Output: 6 concepts, 5 relationships
  │
  └─ 📊 Outputs
     ├─ concepts: 6
     ├─ relationships: 5
     └─ processing_time: 1.52s
```

### Metrics Dashboard
- **Latency trends** - See if your app is getting faster/slower
- **Success rate** - Track reliability
- **Volume** - How many requests per day/hour
- **Error analysis** - See which steps fail most often

---

## 🔍 Useful Filters:

In LangSmith, you can filter by:
- **Date range** - Last hour, day, week
- **Status** - Success vs failures
- **Tags** - Add custom tags to your runs
- **Latency** - Find slow runs
- **Project** - Switch between different projects

---

## 💡 Pro Tips:

1. **Compare runs** - Select multiple runs to compare performance
2. **Export data** - Download metrics as CSV for analysis
3. **Set alerts** - Get notified if latency exceeds threshold
4. **Share traces** - Share specific run URLs with team members

---

## 🎯 Quick Test:

1. **Restart your Streamlit app** (Ctrl+C, then `streamlit run streamlit_app_standalone.py`)
2. Look for: `✅ LangSmith tracing enabled`
3. **Generate a concept map** in the app
4. **Go to https://smith.langchain.com**
5. Click on **`concept-map-generator`** project
6. See your run appear in real-time!

---

## 📞 If You Don't See Metrics:

**Check:**
1. ✅ Did you restart the Streamlit app?
2. ✅ Do you see "LangSmith tracing enabled" in console?
3. ✅ Is your API key correct in `.env`?
4. ✅ Are you logged into the same account at smith.langchain.com?

**Still not working?**
- Check terminal for any LangSmith errors
- Verify API key at: https://smith.langchain.com/settings
- Make sure the project name matches: `concept-map-generator`

---

## 🎉 You're All Set!

Now every time you generate a concept map, you'll see beautiful visualizations and detailed metrics at:

**https://smith.langchain.com**

Enjoy tracking your app's performance! 🚀

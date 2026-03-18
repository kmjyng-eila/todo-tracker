# 📝 Todo Tracker

Daily todo list with focus tracking and weekly analytics. A productivity tool that helps you understand not just what you do, but how well you focus.

**Live Demo:** [https://kmjyng-eila.github.io/todo-tracker/](https://kmjyng-eila.github.io/todo-tracker/)

## ✨ Features

### 🎯 Daily Task Management
- **Task Tracking**: Add, start, hold, resume, and complete tasks
- **Real-time Timer**: Track how long you work on each task
- **Hold System**: Pause work with categorized reasons
  - Preset reasons: 정의 안됨, 의사결정 필요, 외부 요청, 회의, 집중 깨짐, 피로
  - Custom reason input for "기타" option
- **Hold History**: View all pauses with timestamps and durations

### 📊 Focus Score System (0-100 points)
Measures how well you maintain focus, not just how long you work.

**Score Components:**
- **Completion Score (40pts)**: Task completion rate
- **Focus Efficiency (30pts)**: Focus time vs total time ratio
- **Flow Score (20pts)**: Fewer interruptions = higher score
- **Restart Score (10pts)**: Faster resume after holds = higher score

**Status Messages:**
- 80+ points: 🔥 집중 상태 매우 좋음
- 60-79 points: 👍 괜찮음, Hold만 조금 줄이면 더 좋아짐
- 40-59 points: ⚠️ 흐름이 자주 끊김
- 0-39 points: 🚨 재시작 지연 또는 Hold 과다

### 📈 Weekly Analytics
Switch to Weekly view to see:

**Summary Cards:**
- Average Focus Score for the week
- Average completion rate
- Total focus time
- Hold ratio

**Charts:**
- Line chart: Daily focus score trends (Mon-Sun)
- Stacked bar chart: Focus time vs Hold time by day

**Insights:**
- **Top Blockers**: Most frequent hold reasons
- **Restart Behavior**: Average and maximum restart times
- **Task Efficiency**: Average task completion time and hold occurrence rate

### 🔥 Real-time Dashboard
- **Status**: Current task state (IDLE / FOCUS / HOLD / COMPLETED)
- **Focus Time**: Actual working time (excluding holds)
- **Hold Ratio**: Percentage of time spent on hold
- **Progress**: Daily completion rate

### 💾 Data Persistence
- All data saved to localStorage
- Survives browser refresh
- No server required - completely client-side

## 🚀 Usage

### Daily View
1. **Add a task**: Type task name and click "Add Task"
2. **Start working**: Click "Start" button
3. **Hold if needed**: Click "Hold", select reason, confirm
4. **Resume**: Click "Resume" to continue
5. **Finish**: Click "Finish" when done

### Task Details
Each task shows:
- **Focus Time**: Actual working time
- **Hold Time**: Total pause duration
- **Hold Count**: Number of pauses
- **Hold History**: Expandable list of all holds with reasons

### Weekly View
Click "Weekly" tab to see:
- Week summary (Mon-Sun from current week)
- Focus score trends
- Time distribution
- Top blocking reasons
- Efficiency metrics

## 🛠️ Tech Stack

- **HTML5**: Semantic structure
- **CSS3**: Modern responsive design with animations
- **Vanilla JavaScript (ES6+)**: No framework dependencies
- **Chart.js**: Data visualization
- **localStorage**: Client-side data persistence

## 📦 Installation

### Local Development
```bash
# Clone the repository
git clone https://github.com/kmjyng-eila/todo-tracker.git

# Navigate to directory
cd todo-tracker

# Open in browser
open index.html
```

### GitHub Pages
This project is automatically deployed to GitHub Pages. Just push to the main branch.

## 📁 Project Structure

```
todo-tracker/
├── index.html          # Main HTML structure
├── styles.css          # All styling and animations
├── app.js              # Application logic
├── README.md           # Project documentation
└── .gitignore          # Git ignore rules
```

## 🎨 Key Design Features

- **Pulse animation** for active tasks
- **Color-coded states**:
  - Blue: Focus mode
  - Orange: On hold
  - Green: Completed
- **Responsive design**: Works on mobile and desktop
- **Smooth transitions**: Fade-in animations between views
- **Gradient themes**: Modern purple gradient accents

## 📊 Data Structure

```javascript
{
  "2026-03-18": [
    {
      id: 1710765432000,
      text: "Task description",
      completed: false,
      running: false,
      onHold: false,
      startTime: null,
      elapsedTime: 0,
      holdHistory: [
        {
          reason: "회의",
          timestamp: 1710765500000,
          holdStartTime: 1710765500000,
          duration: 300000  // 5 minutes in ms
        }
      ]
    }
  ]
}
```

## 🔮 Future Enhancements

- [ ] Export data to CSV/JSON
- [ ] Task categories/tags
- [ ] Dark mode toggle
- [ ] Task priority levels
- [ ] Monthly statistics view
- [ ] Task notes and descriptions
- [ ] Pomodoro timer integration
- [ ] Multi-device sync

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

**Eila Kim**
- GitHub: [@kmjyng-eila](https://github.com/kmjyng-eila)

## 🙏 Acknowledgments

- Chart.js for beautiful visualizations
- Inspired by productivity and time-tracking tools

---

**Note:** All data is stored locally in your browser. No data is sent to any server. Clear your browser data will delete all tasks.

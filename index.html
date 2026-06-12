<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Habit Tracker Calendar</title>

<style>
    body {
        font-family: Arial, sans-serif;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        background: #f4f6f9;
        margin: 0;
    }

    .container {
        background: white;
        padding: 20px;
        border-radius: 15px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        width: 420px;
    }

    h2 {
        text-align: center;
        margin-bottom: 15px;
    }

    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 15px;
    }

    button {
        padding: 8px 12px;
        border: none;
        background: #4CAF50;
        color: white;
        border-radius: 8px;
        cursor: pointer;
    }

    button:hover {
        background: #45a049;
    }

    .calendar {
        display: grid;
        grid-template-columns: repeat(7, 1fr);
        gap: 6px;
    }

    .day-name {
        font-weight: bold;
        text-align: center;
        padding: 8px;
    }

    .day {
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 8px;
        cursor: pointer;
        background: #eee;
        transition: 0.2s;
    }

    .day:hover {
        background: #ddd;
    }

    .completed {
        background: #4CAF50;
        color: white;
    }

    .empty {
        background: transparent;
        cursor: default;
    }

    .stats {
        text-align: center;
        margin-top: 15px;
        font-weight: bold;
    }
</style>
</head>
<body>

<div class="container">
    <h2>Habit Tracker</h2>

    <div class="header">
        <button onclick="changeMonth(-1)">◀</button>
        <h3 id="monthYear"></h3>
        <button onclick="changeMonth(1)">▶</button>
    </div>

    <div class="calendar" id="calendar"></div>

    <div class="stats">
        Completed Days: <span id="count">0</span>
    </div>
</div>

<script>
let currentDate = new Date();

function getStorageKey(year, month) {
    return `habit-${year}-${month}`;
}

function loadCompleted(year, month) {
    return JSON.parse(localStorage.getItem(getStorageKey(year, month))) || [];
}

function saveCompleted(year, month, data) {
    localStorage.setItem(getStorageKey(year, month), JSON.stringify(data));
}

function renderCalendar() {
    const calendar = document.getElementById("calendar");
    calendar.innerHTML = "";

    const year = currentDate.getFullYear();
    const month = currentDate.getMonth();

    document.getElementById("monthYear").textContent =
        new Date(year, month).toLocaleString("default", {
            month: "long",
            year: "numeric"
        });

    const dayNames = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
    dayNames.forEach(day => {
        const el = document.createElement("div");
        el.className = "day-name";
        el.textContent = day;
        calendar.appendChild(el);
    });

    const firstDay = new Date(year, month, 1).getDay();
    const daysInMonth = new Date(year, month + 1, 0).getDate();

    let completed = loadCompleted(year, month);

    for (let i = 0; i < firstDay; i++) {
        const empty = document.createElement("div");
        empty.className = "day empty";
        calendar.appendChild(empty);
    }

    for (let day = 1; day <= daysInMonth; day++) {
        const cell = document.createElement("div");
        cell.className = "day";
        cell.textContent = day;

        if (completed.includes(day)) {
            cell.classList.add("completed");
        }

        cell.addEventListener("click", () => {
            if (completed.includes(day)) {
                completed = completed.filter(d => d !== day);
                cell.classList.remove("completed");
            } else {
                completed.push(day);
                cell.classList.add("completed");
            }

            saveCompleted(year, month, completed);
            updateCount(completed.length);
        });

        calendar.appendChild(cell);
    }

    updateCount(completed.length);
}

function updateCount(count) {
    document.getElementById("count").textContent = count;
}

function changeMonth(step) {
    currentDate.setMonth(currentDate.getMonth() + step);
    renderCalendar();
}

renderCalendar();
</script>

</body>
</html>

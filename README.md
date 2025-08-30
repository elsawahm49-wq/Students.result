<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>البحث عن نتيجة الطالب</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      direction: rtl;
      text-align: center;
      background: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    h1 {
      background: #2c3e50;
      color: white;
      padding: 15px;
      margin: 0;
    }
    input {
      padding: 10px;
      margin: 20px 10px;
      width: 250px;
      font-size: 16px;
    }
    button {
      padding: 10px 20px;
      background: #34495e;
      color: white;
      border: none;
      cursor: pointer;
      font-size: 16px;
      border-radius: 5px;
    }
    button:hover {
      background: #2c3e50;
    }
  </style>
</head>
<body>
  <h1>البحث عن نتيجة الطالب</h1>
  <input type="text" id="studentName" placeholder="اكتب اسم الطالب هنا">
  <button onclick="searchStudent()">بحث</button>

  <script>
    // بيانات 20 طالب (٨ حصص × ٣٠)
    const students = {
      "أحمد علي": [28,25,27,29,30,26,28,27],
      "سارة محمد": [20,22,24,21,25,23,22,24],
      "محمود يوسف": [15,18,20,17,16,19,20,18],
      "ندى إبراهيم": [30,30,29,30,28,30,29,30],
      "خالد سمير": [10,12,15,14,11,13,12,10],
      "ريم حسن": [25,24,26,27,28,25,26,24],
      "عمر فؤاد": [18,20,22,19,21,20,22,23],
      "ليلى أحمد": [29,30,30,29,30,30,29,30],
      "محمد سعيد": [14,16,15,17,18,16,15,14],
      "داليا كمال": [23,24,22,25,23,24,22,23],
      "يوسف حمدي": [19,21,20,18,19,20,21,22],
      "هالة سمير": [27,28,29,28,27,29,28,30],
      "سامح عادل": [16,15,17,18,16,15,17,16],
      "فاطمة خالد": [24,25,26,24,25,26,25,24],
      "إياد عمر": [22,20,23,22,21,23,22,20],
      "ملك سامي": [30,29,30,30,29,30,30,29],
      "أدهم جمال": [12,14,13,12,15,14,13,12],
      "صفاء طارق": [26,27,28,27,26,28,27,26],
      "حسن علي": [20,19,21,20,22,21,20,19],
      "هند شريف": [28,29,27,28,29,28,29,28]
    };

    function searchStudent() {
      const name = document.getElementById("studentName").value.trim();

      if (students[name] !== undefined) {
        localStorage.setItem("studentName", name);
        localStorage.setItem("grades", JSON.stringify(students[name]));
        window.location.href = "result.html";
      } else {
        alert("⚠️ الطالب غير موجود");
      }
    }
  </script>
</body>
</html>

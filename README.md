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
    #result {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
    }
    .high { color: green; }
    .medium { color: goldenrod; }
    .low { color: red; }
  </style>
</head>
<body>
  <h1>البحث عن نتيجة الطالب</h1>
  <input type="text" id="studentName" placeholder="اكتب اسم الطالب هنا">
  <button onclick="searchStudent()">بحث</button>

  <div id="result"></div>

  <script>
    // بيانات الطلاب
    const students = {
      "أحمد علي": 29,
      "سارة محمد": 27,
      "محمود يوسف": 20,
      "ليلى خالد": 12,
      "عمر حسن": 18,
      "ندى إبراهيم": 30,
      "خالد سمير": 9,
      "فاطمة عمر": 16,
      "يوسف عادل": 25,
      "هبة شريف": 19,
      "إسلام فاروق": 13,
      "منة الله عماد": 28,
      "محمد طارق": 21,
      "ريم عصام": 11,
      "عبدالله كريم": 17,
      "حنان محمود": 26,
      "أدهم ياسر": 10,
      "شهد وليد": 23,
      "بلال أحمد": 30,
      "إسراء جمال": 22
    };

    function searchStudent() {
      const name = document.getElementById("studentName").value.trim();
      const resultDiv = document.getElementById("result");

      if (students[name] !== undefined) {
        let grade = students[name];
        let cssClass = grade >= 25 ? "high" : grade >= 15 ? "medium" : "low";
        resultDiv.innerHTML = `<span class="${cssClass}">${name} : ${grade} / 30</span>`;
      } else {
        resultDiv.innerHTML = `<span style="color:red">⚠️ الطالب غير موجود</span>`;
      }
    }
  </script>
</body>
</html>

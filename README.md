<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>درجات الطلاب</title>
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
    table {
      margin: 20px auto;
      border-collapse: collapse;
      width: 80%;
      background: white;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
    th, td {
      border: 1px solid #ddd;
      padding: 10px;
    }
    th {
      background: #34495e;
      color: white;
    }
    tr:nth-child(even) {
      background: #f9f9f9;
    }
    tr:hover {
      background: #ecf0f1;
      transition: 0.3s;
    }
    .high {
      color: green;
      font-weight: bold;
    }
    .medium {
      color: goldenrod;
      font-weight: bold;
    }
    .low {
      color: red;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>نتائج الطلاب</h1>
  <table>
    <tr>
      <th>اسم الطالب</th>
      <th>الدرجة</th>
    </tr>
    <tr>
      <td>أحمد علي</td>
      <td class="high">95</td>
    </tr>
    <tr>
      <td>سارة محمد</td>
      <td class="high">88</td>
    </tr>
    <tr>
      <td>محمود يوسف</td>
      <td class="medium">76</td>
    </tr>
    <tr>
      <td>ليلى خالد</td>
      <td class="low">54</td>
    </tr>
  </table>
</body>
</html>

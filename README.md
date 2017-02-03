<?php
$data = file_get_contents('http://university.netology.ru/u/karpova/lesson5/data.json');
$array = json_decode($data, true);
?>

<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>

<body>
    <table>
    <thead>
        <tr>
            <th>Имя</th>
            <th>Фамилия</th>
            <th>Адрес</th>
            <th>Телефон</th>
        </tr>
    </thead>
    <tbody>
<?php
  foreach ($array as $item):
    ?>

        <tr>
            <td><?= $item['firstname'] ?></td>
            <td><?= $item['lastname'] ?></td>
            <td><?= $item['adress'] ?></td>
            <td><?= $item['phoneNumber'] ?></td>
        </tr>
      <?php endforeach; ?>
    </tbody>
    </table>
</body>
</html>

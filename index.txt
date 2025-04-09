<?php
$get = $_GET['get'];
$url = 'https://' . $get;

$urlheads = [
  'http' => [
      'timeout' => 60
  ]
];
$context = stream_context_create($urlheads);
$res = file_get_contents($url, false, $context);
echo $res;
?>

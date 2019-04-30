<html>
<head><title></title><head>
<?php 
  function isCorrect($text){ 
  for($j;$j<strlen($text);$j++){ 
  switch($text[$i]){ 
  case "{":  $test.="{";  break; 
  case "(":  $test.="(";  break; 
  case "[":  $test.="[";  break; 
  case "}": if($test[strlen($test)-1]=="{"){ 
               $test=substr($test,0,strlen($test)-1); 
                         } break; 
  case ")": if($test[strlen($test)-1]=="("){ 
               $test=substr($test,0,strlen($test)-1); 
                         } break; 
  case "]": if($test[strlen($test)-1]=="["){ 
               $test=substr($test,0,strlen($test)-1); 
                         } break; 
  } 
 } 
 if(strlen($test)==0){ 
    echo "Строка корректна!"; 
 }else{ 
    echo "Строка не корректна введена!"; 
 } 
} 
isCorrect("{[[()]]}"); 
 ?>
</html> 

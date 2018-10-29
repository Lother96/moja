<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN"
  "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="pl">
<head>
  <meta http-equiv="Content-type" content="application/xhtml+xml; charset=utf-8" />
  <meta name="Description" content=" Zadanie technologie informacyjne " />
  <meta name="Keywords" content=" Zadanie, technologie, informacyjne " />
  <meta name="Author" content=" Hubert PawĹ‚owski sp. Informatyka Gospodarcza " />
  <meta name="Generator" content="kED" />

  <title> Zadanie Technologie Informacyjne </title>

  <link rel="stylesheet" href="styl.css" type="text/css" />
</head>
<body>
<div id="container">
<div id="gnag">
<div id="naglowek">
<a href="index.html" title="start"><img src="naglowek.png" alt="naglowek" class="naglowek"/></a>
</div>
</div>
<div id="menupoz">
<ul>
	<li><a href="index.html">INCLUDE I REQUIRE</a></li>
  <li><a href="pierwiastkowanie.html">PIERWIASTKOWANIE</a></li>
</ul>

</div>
<div id="srodek">
<div id="zawartosc">
<p id="start">Include() i Require()</p>

<p class="mini_tytul">Include()</p>
<p class="tekst">Instrukcja include() pozwala wczytaÄ‡ plik, ktĂłrego adres zostaĹ‚ podany w jej argumencie. SĹ‚uĹĽy ona do wczytania i wykonania kodu z okreĹ›lonego pliku w trakcie wykonywania skryptu.</p>
<p class="tekst">SkĹ‚adnia instrukcji:</p>
<p class="tekst"><strong>Include()</strong> -  gdzie w nawiasie wpisujemy nazwÄ™ pliku, ktĂłry ma zostaÄ‡ doĹ‚Ä…czony np. Include("plik1.php")</p>

<p class="tytulek">PrzykĹ‚ad</p>
<p class="tekst">Mamy plik, ktĂłrego kod wyglÄ…da nastÄ™pujÄ…co (w body):</p>
<textarea rows="13" cols="50" readonly="readonly">

Pierwsza linia
<?php 
include("tekst1.php"); 
?>
</textarea>
<p class="tekst">Tekst pliku tekst.php wyglÄ…da natomiast tak:</p>
<textarea rows="13" cols="50" readonly="readonly">
Druga linia</textarea>
<p class="tekst">W rezultacie <a href="zad1.php">otrzymamy</a></p>

<p class="tytulek">Include_once()</p>
<p class="tekst"><strong>Include_once()</strong>, rĂłĹĽni siÄ™ od Include() tym, ĹĽe jeĹĽeli kod z pliku zostaĹ‚ juĹĽ doĹ‚Ä…czony, to nie zostanie on doĹ‚Ä…czony ponownie, przy kolejnym obiegu.</p>

<p class="mini_tytul">Require()</p>
<p class="tekst">Instrukcja Require() posiada praktycznie identycznÄ… zasadÄ™ diaĹ‚ania co Include(), lecz rĂłĹĽni siÄ™ kilkoma cechami:</p>
<ol class="tekst">
<li>Instrukcja <strong>Require()</strong>  doĹ‚Ä…cza kod z pliku niezaleĹĽnie od tego, czy speĹ‚nione zostaĹ‚y warunki w instrukcjach warunkowych,</li>
<li>Instrukcja <strong>Include()</strong>  wstawia zawsze aktualnÄ… zawartoĹ›Ä‡ pliku, a <strong>Require()</strong> - tylko dane z pierwszego przebiegu,</li>
<li>Instrukcja <strong>Include()</strong>, podczas prĂłby zaĹ‚Ä…czenia pliku ktĂłry nie istnieje wyda ostrzeĹĽenie, <strong>Require()</strong>  - wyda "Fatal Error", co spowoduje, ĹĽe dziaĹ‚anie skryptu zostanie przerwane.</li>
</ol><br/>

<p class="tekst">SkĹ‚adnia instrukcji:</p>
<p class="tekst"><strong>Require()</strong> - gdzie w nawiasie wpisujemy nazwÄ™ pliku, ktĂłry ma zostaÄ‡ doĹ‚Ä…czony np. require(moj_plik.php)</p>

<p class="tytulek">PrzykĹ‚ad</p>
<p class="tekst"><strong>DziaĹ‚anie instukcji Require():</strong></p>
<p class="tekst">Mamy plik, ktĂłrego zawartoĹ›Ä‡ wyglÄ…da nastÄ™pujÄ…co:</p>
<textarea rows="13" cols="50" readonly="readonly">
<?php

function zadanie_req(){
    require('zad3.php');
    return $zadanie_req;
}

for($a=1;$a<=5;$a++){
    echo zadanie_req()."<br>";
}

</textarea>
<p class="tekst">W pliku zad3.php mamy nastÄ™pujÄ…cy kod:</p>
<textarea rows="13" cols="50" readonly="readonly">
<?php
$zadanie_req = 'linia tekstu';
?>
</textarea>
<p class="tekst">W rezultacie <a href="tekst3.php">otrzymamy</a></p><br/>


<p class="tekst"><strong>PrzykĹ‚ad dziaĹ‚ania Fatal Erroru:</strong></p>
<p class="tekst">Mamy plik.php, w ktĂłrym kod wyglÄ…da nastÄ™pujÄ…co (w body):</p>

<textarea rows="13" cols="50" readonly="readonly">
Pierwsza linia
<?php require("zad2.php"); ?>
</textarea>

<p class="tekst">Natomiast pliku o nazwie zad2.php nie ma. W rezultacie otrzymamy <a href="tekst2.php">nastÄ™pujÄ…cy wynik</a></p><br/>

<p class="tytulek">Require_once()</p>
<p class="tekst">Zasada dziaĹ‚ania <strong>Require_once()</strong> jest identyczna, co require(). JedynÄ… rĂłĹĽnicÄ… jest to, ĹĽe instrukcja sprawdzi, czy plik zostaĹ‚ juĹĽ doĹ‚Ä…czony. JeĹ›li tak - nie bÄ™dzie doĹ‚Ä…czaĹ‚ go ponownie.</p>
</div>
</div>
<div id="stopka">
<p>Copyright by Hubert PawĹ‚owski sp. Informatyka Gospodarcza</p>
</div>
</div>


</body>
</html>


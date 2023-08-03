# P04_Counterfeit_Notes_Detection
<h2><strong><em>Data Analyst Certification by OpenClassrooms, in partnership with&nbsp;ENSAE-ENSAI</em></strong></h2>
<p><em>Detecting counterfeit notes using a classification algorithm<br /></em></p>
<p><em>Skills:</em></p>
<ul>
<li><em>Perform a PCA</em></li>
<li><em>Use a Kmeans type clustering algorithm</em></li>
<li><em>Modeling using logistic regression</em></li>
<li><em>Interpret a PCA</em><em><br /></em></li>
</ul>
<div>&nbsp;</div>
<div>
<h1>D&eacute;tectez des faux billets</h1>
<div data-videotitle="video" data-current-user-id="7132501" data-project-id="147" data-codio-button-label="Acc&eacute;der au code">
<h3>Pr&eacute;requis</h3>
<p>Pour ce projet, il sera n&eacute;cessaire de savoir manipuler des donn&eacute;es en&nbsp;<strong>R</strong>&nbsp;ou en&nbsp;<strong>Python</strong>. &Eacute;galement, vous devrez effectuer une analyse de&nbsp;<strong>statistique descriptive</strong>, ainsi qu'une a<strong>nalyse en composantes principales</strong>, une&nbsp;<strong>classification automatique</strong>, et une mod&eacute;lisation de type&nbsp;<strong>r&eacute;gression logistique</strong>.</p>
<h3>Sc&eacute;nario</h3>
<p>Votre soci&eacute;t&eacute; de consulting informatique vous propose une nouvelle mission au minist&egrave;re de l'Int&eacute;rieur, dans le cadre de la lutte contre la criminalit&eacute; organis&eacute;e, &agrave; l'Office central pour la r&eacute;pression du faux monnayage. Votre mission si vous l'acceptez : cr&eacute;er un algorithme de d&eacute;tection de faux billets.</p>
<p>Vous vous voyez d&eacute;j&agrave; en grand justicier combattant sans rel&acirc;che la criminalit&eacute; organis&eacute;e en pianotant &agrave; mains de ma&icirc;tre votre ordinateur, pour fa&ccedil;onner ce fabuleux algorithme qui traquera la moindre fraude et permettra de mettre &agrave; jour les r&eacute;seaux secrets de faux-monnayeurs ! La classe, non ?</p>
<p>... Bon, si on retombait les pieds sur terre? Travailler pour la police judiciaire, c'est bien, mais vous allez devoir faire appel &agrave; vos connaissances en statistiques, alors on y va !</p>
<h3>Les donn&eacute;es</h3>
<p>La PJ vous transmet un&nbsp;<a href="https://s3-eu-west-1.amazonaws.com/static.oc-static.com/prod/courses/files/parcours-data-analyst/notes.csv">jeu de donn&eacute;es</a>&nbsp;contenant les caract&eacute;ristiques g&eacute;om&eacute;triques de billets de banque. Pour chacun d'eux, nous connaissons :</p>
<ul>
<li>la longueur du billet (en mm) ;</li>
<li>la hauteur du billet (mesur&eacute;e sur le c&ocirc;t&eacute; gauche, en mm) ;</li>
<li>La hauteur du billet (mesur&eacute;e sur le c&ocirc;t&eacute; droit, en mm) ;</li>
<li>la marge entre le bord sup&eacute;rieur du billet et l'image de celui-ci (en mm) ;</li>
<li>la marge entre le bord inf&eacute;rieur du billet et l'image de celui-ci (en mm) ;</li>
<li>la diagonale du billet (en mm).</li>
</ul>
<h3>Votre mission</h3>
<h4>Mission 0</h4>
<p>Afin d'introduire votre analyse, effectuez une br&egrave;ve description des donn&eacute;es (analyses univari&eacute;es et bivari&eacute;es).</p>
<h4>Mission 1</h4>
<p>Vous r&eacute;aliserez une analyse en composantes principales de l'&eacute;chantillon, en suivant toutes ces &eacute;tapes :</p>
<ul>
<li>analyse de l'&eacute;boulis des valeurs propres ;</li>
<li>repr&eacute;sentation des variables par le cercle des corr&eacute;lations ;</li>
<li>repr&eacute;sentation des individus par les plans factoriels ;</li>
<li>analyser de la qualit&eacute; de repr&eacute;sentation et la contribution des individus.</li>
</ul>
<p>Pour chacune de ces &eacute;tapes, commentez les r&eacute;sultats obtenus. La variable donnant la nature Vrai/Faux du billet sera utilis&eacute;e comme variable illustrative.</p>
<h4>Mission 2</h4>
<p>Appliquez un algorithme de classification, puis analysez le r&eacute;sultat obtenu.</p>
<p>Visualisez la partition obtenue dans le premier plan factoriel de l'ACP, puis analysez-la.</p>
<h4>Mission 3</h4>
<p>Mod&eacute;lisez les donn&eacute;es &agrave; l'aide d'une r&eacute;gression logistique. Gr&acirc;ce &agrave; celle-ci, vous cr&eacute;erez un programme capable d'effectuer une pr&eacute;diction sur un billet, c'est-&agrave;-dire de d&eacute;terminer s'il s'agit d'un vrai ou d'un faux billet. Pour chaque billet, votre algorithme de classification devra donner la probabilit&eacute; que le billet soit vrai. Si cette probabilit&eacute; est sup&eacute;rieure ou &eacute;gale &agrave; 0.5, le billet sera consid&eacute;r&eacute; comme vrai. Dans le cas contraire, il sera consid&eacute;r&eacute; comme faux.</p>
<aside data-claire-semantic="warning">
<p>Il vous sera demand&eacute; d'utiliser ce programme lors de votre soutenance !</p>
</aside>
<h3>Livrables</h3>
<p>Le livrable attendu est un fichier .zip contenant :</p>
<ul>
<li>le&nbsp;<strong>code</strong>&nbsp;Python ou R de l&rsquo;analyse compl&egrave;te (un ou plusieurs fichiers) ;</li>
<li>les&nbsp;<strong>graphiques</strong>&nbsp;g&eacute;n&eacute;r&eacute;s par le code, en format image.</li>
</ul>
<aside data-claire-semantic="information">
<p dir="ltr">Pour faciliter votre passage au jury, d&eacute;posez sur la plateforme, dans un dossier nomm&eacute; &ldquo;<em>P6_nom_prenom</em>&rdquo;, tous les livrables du projet. Chaque livrable doit &ecirc;tre nomm&eacute; avec le num&eacute;ro du projet et selon l'ordre dans lequel il appara&icirc;t, par exemple &ldquo;<em>P6_01_code</em>&rdquo;, &ldquo;<em>P6_02_graphiques</em>&rdquo;, et ainsi de suite.</p>
</aside>
<h3>Soutenance</h3>
<p>Lors de la soutenance, l'examinateur vous procurera un fichier CSV contenant 5 caract&eacute;ristiques de billets. Votre programme devra d&eacute;terminer si chacun de ces billets est vrai ou faux, en affichant la probabilit&eacute; associ&eacute;e. Ce fichier sera de la m&ecirc;me forme que celui-ci :&nbsp;<a href="https://s3-eu-west-1.amazonaws.com/static.oc-static.com/prod/courses/files/parcours-data-analyst/example.csv">cliquez pour t&eacute;l&eacute;charger example.csv</a>.</p>
<aside data-claire-semantic="warning">
<p>Dans ce fichier d'exemple, chaque billet poss&egrave;de un identifiant (dans la colonne "id"). V&eacute;rifiez que votre programme affiche bien cet identifiant pour chaque pr&eacute;diction effectu&eacute;e.</p>
</aside>
<aside data-claire-semantic="warning">
<p>Assurez-vous que votre programme puisse bien lire ce fichier et effectuer la pr&eacute;diction pour chacun des billets !</p>
</aside>
<p>&nbsp;La soutenance se d&eacute;roulera comme suit :</p>
<ol>
<li>Pr&eacute;sentation du jeu de donn&eacute;es &amp; br&egrave;ves analyse bivari&eacute;es et univari&eacute;es. (5 minutes)</li>
<li>ACP : d&eacute;tail de l'analyse, avec graphiques &agrave; l'appui. (10 minutes)</li>
<li>Analyse de la classification. (5 minutes)</li>
<li>D&eacute;tail de la mod&eacute;lisation. (5 minutes)</li>
<li>Test du programme avec le jeu de test donn&eacute;&nbsp;par&nbsp;l'&eacute;valuateur. (5 minutes)</li>
<li>S&eacute;ance de questions-r&eacute;ponses &eacute;ventuelle.</li>
</ol>
</div>
<h3>Comp&eacute;tences &eacute;valu&eacute;es</h3>
<ul>
<li>
<div>&nbsp;R&eacute;aliser une ACP</div>
</li>
<li>
<div>&nbsp;Utiliser un algorithme de clustering de type Kmeans</div>
</li>
<li>
<div>&nbsp;Mod&eacute;liser gr&acirc;ce &agrave; la r&eacute;gression logistique</div>
</li>
<li>
<div>&nbsp;Interpr&eacute;ter une ACP</div>
</li>
</ul>
</div>

<h1><span style="color:#2980b9"><strong>Descarga de Datos Bicing</strong></span></h1>

<p>Los datos sobre el servicio de sharing de bicicletas, bicing, est&aacute;n disponibles en la web del Ajuntament de Barcelona,&nbsp;<a href="https://opendata-ajuntament.barcelona.cat/resources/bcn/BicingBCN">https://opendata-ajuntament.barcelona.cat/resources/bcn/BicingBCN</a>&nbsp;.&nbsp;Los datos estan agrupados por meses y comprimidos con el formato <span style="color:#3498db">{year}_{month:02d}_{month_name}_BicingNou_ESTACIONS.7z</span>&nbsp; y se recopilan desde marzo de 2019. Para este proyecto, descargamos todos los datos del periodo marzo 2019 . diciembre 2022, que ser&aacute;n los datos que usaremos para el entrenamiento, los guardamos en formato csv, tambi&eacute;n por meses para su posterior procesamiento.</p>

<p>Cada uno de los ficheros contiene la siguiente informaci&oacute;n y tipo de dato:</p>

<table border="0" cellpadding="1" cellspacing="1" style="width:786px">
	<thead>
		<tr>
			<th scope="col" style="width:239px"><strong>Variable</strong></th>
			<th scope="col" style="width:61px"><strong>Tipo</strong></th>
			<th scope="col" style="width:355px"><strong>Descripci&oacute;n</strong></th>
			<th scope="col" style="width:59px"><strong>Min</strong></th>
			<th scope="col" style="width:74px"><strong>Max</strong></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="width:239px"><strong>station_id</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">Identificador de la estaci&oacute;n</td>
			<td style="width:59px">1</td>
			<td style="width:74px">532</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>num_bikes_available</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">autoexplicativa</td>
			<td style="width:59px">0</td>
			<td style="width:74px">54 &nbsp;/ 198*</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>num_bikes_available_types.mechanical</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">autoexplicativa</td>
			<td style="width:59px">0</td>
			<td style="width:74px">54</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>num_bikes_available_types.ebike</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">autoexplicativa</td>
			<td style="width:59px">0</td>
			<td style="width:74px">41</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>num_docks_available</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">autoexplicativa</td>
			<td style="width:59px">0</td>
			<td style="width:74px">54 &nbsp; / 99*</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>last_reported</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">Tiempo en segundos de cuando se tom&oacute;&nbsp;el registro</td>
			<td style="width:59px">&nbsp;</td>
			<td style="width:74px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>is_charging_station</strong></td>
			<td style="width:61px">bool</td>
			<td style="width:355px">Si la estaci&oacute;n permite cargar bicis el&eacute;ctricas</td>
			<td style="width:59px">&nbsp;</td>
			<td style="width:74px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>status</strong></td>
			<td style="width:61px">object</td>
			<td style="width:355px">
			<pre>
IN_SERVICE        
MAINTENANCE       
PLANNED 
NOT_IN_SERVICE  
END_OF_LIFE
</pre>
			</td>
			<td style="width:59px">&nbsp;</td>
			<td style="width:74px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>is_installed</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">Si la estaci&oacute;n est&aacute; instalada</td>
			<td style="width:59px">0</td>
			<td style="width:74px">1</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>is_renting</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">Si la estaci&oacute;n permite la entrega(desbloquo) de bicicletas</td>
			<td style="width:59px">0</td>
			<td style="width:74px">1</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>is_returning</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">Si la estaci&oacute;n permite la devoluci&oacute;n de bicicletas</td>
			<td style="width:59px">0</td>
			<td style="width:74px">1</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>last_updated</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">Tiempo en segundos de la &uacute;ltima actualizaci&oacute;n&nbsp;</td>
			<td style="width:59px">&nbsp;</td>
			<td style="width:74px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:239px">
			<p><strong>traffic (a partir de finales de 2021)</strong></p>
			</td>
			<td style="width:61px">float64</td>
			<td style="width:355px">Desconocemos su significado, pero en la mayor&iacute;a de casos o no est&aacute; disponible o contiene NAN</td>
			<td style="width:59px">&nbsp;</td>
			<td style="width:74px">&nbsp;</td>
		</tr>
		<tr>
			<td style="width:239px"><strong>ttl</strong></td>
			<td style="width:61px">int64</td>
			<td style="width:355px">Variable descartable para este proyecto</td>
			<td style="width:59px">&nbsp;</td>
			<td style="width:74px">
			<p>&nbsp;</p>
			</td>
		</tr>
	</tbody>
</table>

<p>Debido al gran tama&ntilde;o de los ficheros, en un primer paso concatenamos los ficheros mensuales&nbsp;agrupando&nbsp;la informaci&oacute;n por a&ntilde;os, salvando cada a&ntilde;o en un fichero csv, y procedemos a analizar los datos a&ntilde;o por a&ntilde;o para ver qu&eacute; tipo de datos tenemos&nbsp;y hacer un primer procesado&nbsp;descartando&nbsp;aquellas variables que consideremos innecesarias para este proyecto o transformando algunas de ellas.</p>

<p>Hacemos las siguientes observaciones:</p>

<ul>
	<li>La variable <strong>last_reported</strong> no tiene registro en algunos casos (en 2019 por ejemplo). La descartaremos.</li>
	<li>Nos quedamos con la variable <strong>last_udpated</strong>&nbsp;para saber en qu&eacute; momento se tomaron los datos, cambiaremos el formato a la fecha y hora correspondiente a&nbsp;nuestra zona horaria&nbsp;(timezone&nbsp;Europe/Madrid) creando&nbsp;las nuevas variables: <strong>year, month, day, hour, min</strong></li>
	<li>Las variables <strong>ttl</strong>&nbsp;y&nbsp;<strong>traffic</strong> tambi&eacute;n las descartaremos. Est&aacute; &uacute;ltima variable no est&aacute; recogida durante los primeros a&ntilde;os, se incorpora a finalesl de 2021, pero en la mayoria de casos contine NAN</li>
	<li>Interpretamos los posibles valores de la variable <strong>status</strong> de la siguiente manera:
	<ul>
		<li>IN_SERVICE: estaci&oacute;n en pleno funcionamiento</li>
		<li>NOT_IN_SERVICE: estaci&oacute;n temporalmente fuera de servicio. Puede ser por unas horas debido a alg&uacute;n evento o por varios dias debido a obras en la zona</li>
		<li>MAINTENANCE: la estaci&oacute;n est&aacute; siendo asistida por el servicio de bicing, a&ntilde;adiendo o sustrayendo las bicicletas disponible en esa estaci&oacute;n. Ese proceso dura unos minutos</li>
		<li>PLANNED: estaci&oacute;n planificada pero todavia no est&aacute; en servicio.&nbsp;</li>
		<li>END_OF_LIFE: estaci&oacute;n suprimida</li>
	</ul>
	</li>
</ul>

<p style="margin-left:40px">Tambi&eacute;n observamos que el&nbsp;n&uacute;mero de [&nbsp;NOT_IN_SERVICE + MAINTENANCE + PLANNED] &nbsp;equivale al n&uacute;mero de &nbsp;[<strong>is_returning</strong>==0] ; y que&nbsp;el n&uacute;mero de [PLANNED] equivale al n&uacute;mero [<strong>is_installed</strong>==0].&nbsp;</p>

<p style="margin-left:40px">Tambi&eacute;n vemos que cuando las estaciones tienen un estado distinto a IN_SERVICE los datos &nbsp;sobre <strong>num_bikes_available</strong>, <strong>num_bikes_available_types.ebike</strong>, <strong>num_bikes_available_types.mechanical</strong> y <strong>num_docks_available</strong> tienen inconsistencias. En la mayoria de casos num_bikes_available est&aacute; a cero cuando el detalle bicicletas el&eacute;ctricas y mec&aacute;nicas dice lo contrario; y tambi&eacute;n hay varios casos con num_bike_available y num_docks_available ambos a cero. Adem&aacute;s en esos casos no es posible devolver bicicletas como acabamos de comentar arriba, por lo que a efectos pr&aacute;cticos no hay docks disopnibles para el usuario. Por todo ello procederemos a eliminar los records en los que <strong>status</strong> != IN_SERVICE</p>

<ul>
	<li>Detectamos 205 casos con datos incorrectos&nbsp;(todos los valores de bicicleta tienen el valor 99* &oacute;&nbsp;198*,claramente valores fuera de rango)&nbsp;de estaciones aparentemente en servicio en el <strong>a&ntilde;o 2020, </strong>y alguno en <strong>2021</strong>. Procedemos a eliminarlos</li>
</ul>

<table border="1" cellpadding="1" cellspacing="1" style="width:992px">
	<tbody>
		<tr>
			<td style="width:982px">
			<p>Out[43]:</p>

			<table border="1">
				<thead>
					<tr>
						<th>&nbsp;</th>
						<th>station_id</th>
						<th>num_bikes_available</th>
						<th>num_bikes_available_types.mechanical</th>
						<th>num_bikes_available_types.ebike</th>
						<th>num_docks_available</th>
						<th>is_installed</th>
						<th>is_renting</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<th>1110164</th>
						<td>529</td>
						<td>198</td>
						<td>99</td>
						<td>99</td>
						<td>99</td>
						<td>1</td>
						<td>1</td>
					</tr>
					<tr>
						<th>1110652</th>
						<td>529</td>
						<td>198</td>
						<td>99</td>
						<td>99</td>
						<td>99</td>
						<td>1</td>
						<td>1</td>
					</tr>
					<tr>
						<th>...</th>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
					</tr>
					<tr>
						<th>4386792</th>
						<td>529</td>
						<td>198</td>
						<td>99</td>
						<td>99</td>
						<td>99</td>
						<td>1</td>
						<td>1</td>
					</tr>
					<tr>
						<th>4387298</th>
						<td>529</td>
						<td>198</td>
						<td>99</td>
						<td>99</td>
						<td>99</td>
						<td>1</td>
						<td>1</td>
					</tr>
				</tbody>
			</table>

			<p>205 rows &times; 13 columns</p>
			</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>

<p>Por &uacute;ltimo vemos que quedan algunos casos donde num_bikes_available y num_docks_available ambos est&aacute;n a cero, cuando la estaci&oacute;n est&aacute; IN_SERVICE. Esos casos en lugar de eliminarlos los estamos considerando como estaciones que no aceptan la devoluci&oacute;n de bicicletas, como si estuvieran llenas.</p>

<table border="1" cellpadding="1" cellspacing="1" style="width:500px">
	<tbody>
		<tr>
			<td>
			<table border="1">
				<thead>
					<tr>
						<th>&nbsp;</th>
						<th>station_id</th>
						<th>num_bikes_available</th>
						<th>num_bikes_available_types.mechanical</th>
						<th>num_bikes_available_types.ebike</th>
						<th>num_docks_available</th>
						<th>status</th>
						<th>is_renting</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<th>657079</th>
						<td>79</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>IN_SERVICE</td>
						<td>1</td>
					</tr>
					<tr>
						<th>659099</th>
						<td>79</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>IN_SERVICE</td>
						<td>1</td>
					</tr>
					<tr>
						<th>...</th>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
						<td>...</td>
					</tr>
					<tr>
						<th>1643723</th>
						<td>148</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>IN_SERVICE</td>
						<td>1</td>
					</tr>
					<tr>
						<th>2075695</th>
						<td>394</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>0</td>
						<td>IN_SERVICE</td>
						<td>1</td>
					</tr>
				</tbody>
			</table>

			<p>9591 rows &times; 13 columns</p>
			</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>

<p>El formato de los ficheros .csv que guardamos con las informaci&oacute;n anual sobre el bicing,&nbsp;<strong>Bicing_{year}.csv,</strong>&nbsp;contendr&aacute; esta informaci&oacute;n:</p>

<table border="1" cellpadding="1" cellspacing="1" style="width:998px">
	<thead>
		<tr>
			<th scope="col" style="width:72px">station_id</th>
			<th scope="col" style="width:147px">num_bikes_available</th>
			<th scope="col" style="width:241px"><strong>num_bikes_available_types.mechanical</strong></th>
			<th scope="col" style="width:212px"><strong>num_bikes_available_types.ebike</strong></th>
			<th scope="col" style="width:147px">num_docks_available</th>
			<th scope="col" style="width:33px">year</th>
			<th scope="col" style="width:32px">month</th>
			<th scope="col" style="width:40px">day</th>
			<th scope="col" style="width:42px">hour</th>
			<th scope="col" style="width:41px">min</th>
		</tr>
	</thead>
	<tbody>
	</tbody>
</table>

<p>Estos ficheros ser&aacute;n los que usaremos para analizar con m&aacute;s detalle qu&eacute; ocurri&oacute; en 2020 y c&oacute;mo funciona el bicing en la actualidad,&nbsp;2022, mostrando gr&aacute;ficas y mapas&nbsp;coloreads din&aacute;micamente.</p>

<p>Una de las principales observaciones es la diferencia de n&uacute;mero de registros incluidos cada a&ntilde;o: los a&ntilde;os 2021 y 2020 tienes n&uacute;mero de registros similares; el a&ntilde;o 2019, cuando empez&oacute; el registro, tiene algo menos, como si los registros estuvieran m&aacute;s espaciados en el tiempo; y el a&ntilde;o 2020 tiene menos debido principalmente a la pandemia, cuando durante unas semanas el servicio se lleg&oacute; incluso a interrumpir totalmente (mediados de marzo a finales de abril).</p>

<p><img src=" https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura1_2019.png" style="height:278px; width:350px" /><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura1_2020.png" style="height:285px; width:350px" /></p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura1_2021.png" style="height:285px; width:350px" /><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura2_2022.png" style="height:285px; width:350px" /></p>

<h2><span style="color:#2980b9">Descarga megadatos de las estaciones</span>&nbsp;</h2>

<p>La informaci&oacute;n de cada estaci&oacute;n en el a&ntilde;o 2023, ubicaci&oacute;n, direcci&oacute;n, capacidad, etc, est&aacute; disponible en la web del ayuntamiento, en formato json. Descargamos el fichero, que contiene:</p>

<pre>
RangeIndex: 505 entries, 0 to 504
Data columns (total 14 columns):
 #   Column                  Non-Null Count  Dtype  
---  ------                  --------------  -----  
<strong> 0   station_id              505 non-null    int64  </strong>
<strong> 1   name                    505 non-null    object</strong> 
<span style="color:#999999"> 2   physical_configuration  505 non-null    object</span> 
<strong> 3   lat                     505 non-null    float64
 4   lon                     505 non-null    float64
 5   altitude                505 non-null    float64
 6   address                 505 non-null    object 
 7   post_code               505 non-null    object 
 8   capacity                505 non-null    int64</strong>  
<span style="color:#999999"> 9   is_charging_station     505 non-null    bool   
 10  nearby_distance         505 non-null    float64
 11  _ride_code_support      505 non-null    bool   
 12  rental_uris             0 non-null      object 
 13  cross_street            1 non-null      object </span>
dtypes: bool(2), float64(4), int64(2), object(6)</pre>

<p>y eliminamos los campos que no nos interesan (las marcadas en gris)&nbsp;&nbsp;y guardamos el resto en formato .csv para us uso posterior, por ejemplo filtrar los datos de los a&ntilde;os a entrenar para que incluyan solo las estaciones v&aacute;lidas en 2023.</p>

<p><strong>WARNING ,&nbsp;</strong>vemos que una de las estaciones no tiene informaci&oacute;n sobre la capacidad,. Buscamos dicha informaci&oacute;n, complementamos el dato y guardamos como&nbsp;<strong>Informacio_Estacions_Bicing.csv</strong></p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura3_missingcapacity.png" style="height:90px; width:600px" /></p>

<h2><span style="color:#2980b9">Postproceso de los datos para el training</span></h2>

<p>Recuperamos los ficheros .csv por a&ntilde;o que hab&iacute;amos generado, concatenamos para obtener un &uacute;nico dataframe y seguimos con las transformaciones para obtener un dataframe de este tipo</p>

<table border="1" cellpadding="1" cellspacing="1" style="width:500px">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th>station_id</th>
			<th>year</th>
			<th>month</th>
			<th>day</th>
			<th>hour</th>
			<th>capacity</th>
			<th>altitude</th>
			<th>percentage_docks_available</th>
			<th>ctx-4</th>
			<th>ctx-3</th>
			<th>ctx-2</th>
			<th>ctx-1</th>
		</tr>
		<tr>
			<th>0</th>
			<td>1</td>
			<td>2019</td>
			<td>3</td>
			<td>28</td>
			<td>22</td>
			<td>46.0</td>
			<td>16.0</td>
			<td>0.021739</td>
			<td>0.304348</td>
			<td>0.280435</td>
			<td>0.244565</td>
			<td>0.054348</td>
		</tr>
		<tr>
			<th scope="col">&nbsp;</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
			<th scope="col">...</th>
		</tr>
	</thead>
	<tbody>
	</tbody>
</table>

<p><span style="color:#2980b9">&nbsp;</span></p>

<h3><span style="color:#2980b9">Filtrado estaciones operativas en 2023</span></h3>

<p>Filtramos los datos para quedarnos s&oacute;lo con aquellos que correspondan a estaciones operativas en 2023 y en los a&ntilde;o anteriores.</p>

<h3><span style="color:#2980b9">C&aacute;lculo variable target</span></h3>

<ul>
	<li>Recuperamos el .csv con los metadatos de las estaciones y hacemos merge con el dataframe base para quedarnos con la capacidad.</li>
	<li>Creamos la variable target, <strong>percentage_docks_available</strong> como el porcentage de&nbsp;<strong>num_docks_available</strong>&nbsp; respecto la&nbsp;<strong>capacity </strong>de la estaci&oacute;n. Detectamos peque&ntilde;os errores, en algunos casos el n&uacute;mero de docks es algo mayo que la capacidad y reajustamos el porcentage a 1</li>
</ul>

<table align="left" border="1" cellpadding="1" cellspacing="1" style="width:691px">
	<thead>
		<tr>
			<th>
			<p style="margin-left:40px">&nbsp;</p>
			</th>
			<th>station_id</th>
			<th>year</th>
			<th>month</th>
			<th style="width:22px">day</th>
			<th style="width:26px">hour</th>
			<th>num_docks_available</th>
			<th>capacity</th>
			<th style="width:223px">percentage_docks_available</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>1034369</th>
			<td>11</td>
			<td>2022</td>
			<td>1</td>
			<td style="width:22px">11</td>
			<td style="width:26px">20</td>
			<td>35</td>
			<td>34</td>
			<td style="width:223px">1.029412</td>
		</tr>
		<tr>
			<th>1035483</th>
			<td>11</td>
			<td>2022</td>
			<td>1</td>
			<td style="width:22px">15</td>
			<td style="width:26px">18</td>
			<td>35</td>
			<td>34</td>
			<td style="width:223px">1.029412</td>
		</tr>
	</tbody>
</table>

<pre>
&nbsp;</pre>

<p>&nbsp;</p>

<p>&nbsp;</p>

<p style="margin-left:40px">&nbsp;</p>

<p style="margin-left:40px">Solucionamos con esta instrucci&oacute;n,</p>

<p style="margin-left:80px">dftotrain22.loc[(dftotrain22.percentage_docks_available &gt; 1),&#39;percentage_docks_available&#39;]=1</p>

<ul>
	<li>Eliminamos la columnas que no necesitaremos:&nbsp;<strong>num_bikes_available</strong>,&nbsp;<strong>num_bikes_available_types.mechanical</strong>,&nbsp;<strong>num_bikes_available_types.ebike</strong>, <strong>num_docsk_available</strong>,&nbsp;<strong>min</strong></li>
</ul>

<h3><span style="color:#2980b9">C&aacute;lculo columnas ctx-4, ctx-3, ctx-2, ctx-1</span></h3>

<p>Con el objetivo de reducir el tama&ntilde;o de los ficheros se propone en este caso a&ntilde;adir como variables lo porcentage de dock disponibles las horas previas, hasta 4 horas antes</p>

<ul>
	<li>df=df.groupby([&#39;station_id&#39;,&#39;year&#39;,&#39;month&#39;,&#39;day&#39;,&#39;hour&#39;],as_index=False).mean(numeric_only=True)&nbsp;</li>
	<li>a&ntilde;adimos las columnas basadas en los porcentages anteriores<br />
	&nbsp; &nbsp; df[&#39;ctx-4&#39;] = df[&#39;percentage_docks_available&#39;].shift(periods=4, fill_value=0)<br />
	&nbsp; &nbsp; df[&#39;ctx-3&#39;] = df[&#39;percentage_docks_available&#39;].shift(periods=3, fill_value=0)<br />
	&nbsp; &nbsp; df[&#39;ctx-2&#39;] = df[&#39;percentage_docks_available&#39;].shift(periods=2, fill_value=0)<br />
	&nbsp; &nbsp; df[&#39;ctx-1&#39;] = df[&#39;percentage_docks_available&#39;].shift(periods=1, fill_value=0)</li>
	<li>eliminamos las filas intermedias puesto que la informaci&oacute;n ya se tiene en las variables adicionales&nbsp;<br />
	&nbsp; &nbsp; df_length, initial_row, row_increase = df.shape[0], 4, 5<br />
	&nbsp; &nbsp; df = df.iloc[initial_row:df_length:row_increase]</li>
</ul>

<p>Ahora tenemos esto:</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura4_trainformat.png" style="height:173px; width:800px" /></p>

<p>y la correspondiente descripci&oacute;n, cuyos valores nos parecen razonables:</p>

<table border="1">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th>station_id</th>
			<th>year</th>
			<th>month</th>
			<th>day</th>
			<th>hour</th>
			<th>capacity</th>
			<th>altitude</th>
			<th>percentage_docks_available</th>
			<th>ctx-4</th>
			<th>ctx-3</th>
			<th>ctx-2</th>
			<th>ctx-1</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>count</th>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
			<td>2.972606e+06</td>
		</tr>
		<tr>
			<th>mean</th>
			<td>2.505664e+02</td>
			<td>2.020710e+03</td>
			<td>6.914189e+00</td>
			<td>1.576251e+01</td>
			<td>1.151709e+01</td>
			<td>2.703986e+01</td>
			<td>3.388781e+01</td>
			<td>5.772495e-01</td>
			<td>5.771808e-01</td>
			<td>5.771795e-01</td>
			<td>5.771876e-01</td>
			<td>5.771720e-01</td>
		</tr>
		<tr>
			<th>std</th>
			<td>1.447714e+02</td>
			<td>1.070144e+00</td>
			<td>3.351605e+00</td>
			<td>8.807712e+00</td>
			<td>6.921322e+00</td>
			<td>6.407054e+00</td>
			<td>3.114515e+01</td>
			<td>2.858497e-01</td>
			<td>2.859283e-01</td>
			<td>2.858136e-01</td>
			<td>2.858224e-01</td>
			<td>2.858770e-01</td>
		</tr>
		<tr>
			<th>min</th>
			<td>1.000000e+00</td>
			<td>2.019000e+03</td>
			<td>1.000000e+00</td>
			<td>1.000000e+00</td>
			<td>0.000000e+00</td>
			<td>1.200000e+01</td>
			<td>2.000000e+00</td>
			<td>0.000000e+00</td>
			<td>0.000000e+00</td>
			<td>0.000000e+00</td>
			<td>0.000000e+00</td>
			<td>0.000000e+00</td>
		</tr>
		<tr>
			<th>25%</th>
			<td>1.260000e+02</td>
			<td>2.020000e+03</td>
			<td>4.000000e+00</td>
			<td>8.000000e+00</td>
			<td>6.000000e+00</td>
			<td>2.400000e+01</td>
			<td>8.000000e+00</td>
			<td>3.589744e-01</td>
			<td>3.589744e-01</td>
			<td>3.589744e-01</td>
			<td>3.589744e-01</td>
			<td>3.583333e-01</td>
		</tr>
		<tr>
			<th>50%</th>
			<td>2.500000e+02</td>
			<td>2.021000e+03</td>
			<td>7.000000e+00</td>
			<td>1.600000e+01</td>
			<td>1.200000e+01</td>
			<td>2.700000e+01</td>
			<td>2.400000e+01</td>
			<td>6.200000e-01</td>
			<td>6.203704e-01</td>
			<td>6.201923e-01</td>
			<td>6.203704e-01</td>
			<td>6.200000e-01</td>
		</tr>
		<tr>
			<th>75%</th>
			<td>3.700000e+02</td>
			<td>2.022000e+03</td>
			<td>1.000000e+01</td>
			<td>2.300000e+01</td>
			<td>1.800000e+01</td>
			<td>3.000000e+01</td>
			<td>4.900000e+01</td>
			<td>8.240741e-01</td>
			<td>8.240741e-01</td>
			<td>8.240741e-01</td>
			<td>8.240741e-01</td>
			<td>8.240741e-01</td>
		</tr>
		<tr>
			<th>max</th>
			<td>5.190000e+02</td>
			<td>2.023000e+03</td>
			<td>1.200000e+01</td>
			<td>3.100000e+01</td>
			<td>2.300000e+01</td>
			<td>5.400000e+01</td>
			<td>1.660000e+02</td>
			<td>1.000000e+00</td>
			<td>1.000000e+00</td>
			<td>1.000000e+00</td>
			<td>1.000000e+00</td>
			<td>1.000000e+00</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>

<p>Por &uacute;ltimo, guardamos el fichero de training en formato csv con el nombre&nbsp;<strong>Bicing_ToTrain.csv </strong>para el poterior an&aacute;lisis,&nbsp;postproceso (a&ntilde;adir m&aacute;s variables), entrenamiento y finalmente selecci&oacute;n del modelo:</p>

<h2><span style="color:#2980b9">Carga datos meteorol&oacute;gicos</span></h2>

<p>Creemos que disponer de algunos datos meteorol&oacute;gicos para el entrenamiento del modelo pueden ser de ayuda. Para ello accedemos a los datos hist&oacute;ricos publicados por Meteocat, no s&oacute;n p&uacute;blicos pero se da acceso gratuito temporal para uso educativo, no lucrativo.&nbsp;</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura0_observatoris.png" style="height:369px; width:600px" /></p>

<p>En Barcelona hay las siguientes estaciones meteorol&oacute;gicas automatizadas:</p>

<ul>
	<li>Barcelona - el Raval: &#39;X4&#39;</li>
	<li>Barcelona Zona Universitaria: &#39;X8&#39;</li>
	<li>Barcelona - Observatori Fabra (Tibidabo): &#39;D5&#39;</li>
	<li>Barcelona - Zoo (Ciutadella): &#39;X2&#39; (nom&eacute;s t&eacute; variables sobre temperatura i humitat :( )</li>
	<li>Port de Barcelona - Bocana Sud: &#39;Y7&#39; (al Prat de Llobregat)</li>
	<li>Port de Barcelona - ZAL Prat: &#39;Y9&#39; (al Prat de Llobregat)</li>
</ul>

<p>Dadas las ubicaciones de las estaciones de bicing, descartamos las ubicadas en el puerto de Barcelona. Tambi&eacute;n descartamos la del Zoo de Barcelona puesto que solo recoge un par de datos: temperatura y humedad relativa. Nos descargamos de la web de meteocat los metadatos de las variables y de las estaciones meteorol&oacute;gicas para poder definir correctamente la URL de descarga e interpretar los valores de las variables meteorol&oacute;gicas.</p>

<p>Los datos se ofrecen para un dia y estaci&oacute;n determinados (cada estaci&oacute;n tiene un c&oacute;digo). Procederemos a descargar los datos para todo el perido de entrenamiento, de marzo 2019 a diciembre de 2022, y luego para el set de predicci&oacute;n (primer trimestre de 2023) usando el c&oacute;digo python:</p>

<p style="margin-left:40px">import requests</p>

<p style="margin-left:40px">key = &#39;LaClaveProporcionadaPorMeteocat&#39;;<br />
url0 = &#39;https://api.meteo.cat/xema/v1/estacions/mesurades&#39;</p>

<p style="margin-left:40px"><strong>def get_meteocat_day_data</strong>(codi, year, month, day):<br />
&nbsp; &nbsp; &quot;&quot;&quot;<br />
&nbsp; &nbsp; Function that downloads the data for a specific day of the year from meteocat website, converts it&nbsp;<br />
&nbsp; &nbsp; to a DataFrame and saves it to a csv file for future use. &nbsp;Sample of URL:</p>

<pre style="margin-left:40px">
   <span style="font-size:12px"> <span style="color:#3498db">https://api.meteo.cat/xema/v1/estacions/mesurades/X2/2022/02/01</span></span></pre>

<p style="margin-left:40px">&nbsp; &nbsp; NOTE: the number of queries to meteocat site is limited in the time, hence we save the info in csv files<br />
&nbsp; &nbsp; &quot;&quot;&quot;<br />
&nbsp; &nbsp; url_i = url0+&#39;/{}/{}/{:02d}/{:02d}&#39;.format(codi,year,month,day)<br />
&nbsp; &nbsp; print(url_i)<br />
&nbsp; &nbsp; response_i = requests.get(url_i, headers={&quot;Content-Type&quot;: &quot;application/json&quot;, &quot;X-Api-Key&quot;: key})</p>

<p style="margin-left:40px">&nbsp; &nbsp; assert (response_i.status_code == 200), f&quot;response status code: {response_i.status_code}&quot;<br />
&nbsp; &nbsp;&nbsp;<br />
&nbsp; &nbsp; dbmet = pd.read_json(response_i.text)<br />
&nbsp; &nbsp; <strong>return</strong> &nbsp;pd.json_normalize(dbmet[&#39;variables&#39;][0], record_path=[&#39;lectures&#39;],meta=[&#39;codi&#39;])</p>

<p>Vamos leyendo la informaci&oacute;n por dia y estaci&oacute;n y la guardamos agrupadas por meses, para mantener el paralelismo con los datos del bicing, con el formato&nbsp;{year}/{year}_{month:02d}_MeteoBCN{name}_{code}.csv</p>

<h3><span style="color:#2980b9">Procesado datos meteorol&oacute;gicos</span></h3>

<p>Los datos nos llegan con este formato, donde codi es el identificador de la variable meteorol&oacute;gica medida, y la base horaria es cada 30 minutos:</p>

<table border="\&quot;1\&quot;">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th>data</th>
			<th>dataExtrem</th>
			<th>valor</th>
			<th>estat</th>
			<th>baseHoraria</th>
			<th>codi</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>0</th>
			<td>2020-12-01T00:00Z</td>
			<td>2020-12-01T00:00Z</td>
			<td>1018.6</td>
			<td>V</td>
			<td>SH</td>
			<td>1</td>
		</tr>
		<tr>
			<th>1</th>
			<td>2020-12-01T00:30Z</td>
			<td>2020-12-01T00:37Z</td>
			<td>1018.5</td>
			<td>V</td>
			<td>SH</td>
			<td>1</td>
		</tr>
		<tr>
			<th>2</th>
			<td>2020-12-01T01:00Z</td>
			<td>2020-12-01T01:11Z</td>
			<td>1018.4</td>
			<td>V</td>
			<td>SH</td>
			<td>1</td>
		</tr>
		<tr>
			<th>...</th>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
		</tr>
		<tr>
			<th>1005</th>
			<td>2020-12-31T22:30Z</td>
			<td>2020-12-31T22:30Z</td>
			<td>0.0</td>
			<td>V</td>
			<td>SH</td>
			<td>72</td>
		</tr>
		<tr>
			<th>1006</th>
			<td>2020-12-31T23:00Z</td>
			<td>2020-12-31T23:00Z</td>
			<td>0.0</td>
			<td>V</td>
			<td>SH</td>
			<td>72</td>
		</tr>
		<tr>
			<th>1007</th>
			<td>2020-12-31T23:30Z</td>
			<td>2020-12-31T23:30Z</td>
			<td>0.0</td>
			<td>V</td>
			<td>SH</td>
			<td>72</td>
		</tr>
	</tbody>
</table>

<p>La fecha est&aacute; en formato UTC, por lo que tendremos que convertirla a formato time zone Europe/Madrid para mantener la coherencia con&nbsp;&nbsp;los datos del Bicing y poder concatenarlos correctamente..</p>

<p>Nos aseguramos que todos los datos estan verificados.&nbsp;De las m&aacute;s de 20 variables meteorol&oacute;gicas que se recogen por estaci&oacute;n, usaremos solo las siguientes:</p>

<table border="1" cellpadding="1" cellspacing="1" style="width:410px">
	<thead>
		<tr>
			<th scope="col">Nombre</th>
			<th scope="col" style="width:71px">Unidades</th>
			<th scope="col" style="width:82px">Acr&oacute;nimo</th>
			<th scope="col" style="width:89px">C&oacute;digo</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>Presi&oacute;n atmosf&eacute;rica</td>
			<td style="width:71px">hPA</td>
			<td style="width:82px">P</td>
			<td style="width:89px">34</td>
		</tr>
		<tr>
			<td>Temperatura</td>
			<td style="width:71px">&ordm;C</td>
			<td style="width:82px">T</td>
			<td style="width:89px">32</td>
		</tr>
		<tr>
			<td>Humedad relativa</td>
			<td style="width:71px">%</td>
			<td style="width:82px">HR</td>
			<td style="width:89px">33</td>
		</tr>
		<tr>
			<td>Precipitaci&oacute;n</td>
			<td style="width:71px">mm</td>
			<td style="width:82px">PPT</td>
			<td style="width:89px">35</td>
		</tr>
		<tr>
			<td>Velocidad viento</td>
			<td style="width:71px">m/s</td>
			<td style="width:82px">VV10</td>
			<td style="width:89px">30</td>
		</tr>
		<tr>
			<td>Direcci&oacute;n viento</td>
			<td style="width:71px">&ordm;</td>
			<td style="width:82px">DV10</td>
			<td style="width:89px">31</td>
		</tr>
		<tr>
			<td>Irradiancia solar</td>
			<td style="width:71px">W/m&sup2;</td>
			<td style="width:82px">&nbsp;</td>
			<td style="width:89px">36</td>
		</tr>
	</tbody>
</table>

<p>Recuperamos los datos salvados mensualmente por estaci&oacute;n, los concatenamos agrupados por estaci&oacute;n, &nbsp;descartamos dataExtrem, estat, y baseHoraria pues ya no los necesitamos, agrupamos los datos por fecha y hora ,&nbsp;pivotamos la tabla para que las variables queden como columnas, &nbsp;reemplazamos los c&oacute;digos (num&eacute;ricos) por el acr&oacute;nimo correspondiente,&nbsp;y salvamos temporalmente en un dataframe por estaci&oacute;n.</p>

<p>Por &uacute;ltimo unificamos en un solo dataframe, calculando la media de las tres estaciones consideradas y salvamos en un fichero para posterior uso, con el nombre <strong>All_MeteoBCN.csv</strong></p>

<p>Para el training s&oacute;lo usaremos los datos que van de marzo 2019 a dicembre 2022, mientras que los del primer trimestre de 2023 se dejaran para la predicci&oacute;n.</p>

<p>Cuando unamos estos datos a los del training tendr&aacute; este aspecto:</p>

<table border="\&quot;1\&quot;">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th>year</th>
			<th>month</th>
			<th>day</th>
			<th>hour</th>
			<th>RS</th>
			<th>PPT</th>
			<th>P</th>
			<th>HR</th>
			<th>T</th>
			<th>DV10</th>
			<th>VV10</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>0</th>
			<td>2019</td>
			<td>3</td>
			<td>1</td>
			<td>0</td>
			<td>0.0</td>
			<td>0.0</td>
			<td>1003.600000</td>
			<td>80.666667</td>
			<td>12.000000</td>
			<td>197.333333</td>
			<td>1.200000</td>
		</tr>
		<tr>
			<th>1</th>
			<td>2019</td>
			<td>3</td>
			<td>1</td>
			<td>1</td>
			<td>0.0</td>
			<td>0.0</td>
			<td>1003.566667</td>
			<td>77.000000</td>
			<td>12.100000</td>
			<td>195.000000</td>
			<td>0.700000</td>
		</tr>
		<tr>
			<th>2</th>
			<td>2019</td>
			<td>3</td>
			<td>1</td>
			<td>2</td>
			<td>0.0</td>
			<td>0.0</td>
			<td>1003.466667</td>
			<td>79.000000</td>
			<td>11.633333</td>
			<td>250.666667</td>
			<td>0.900000</td>
		</tr>
		<tr>
			<th>...</th>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
		</tr>
		<tr>
			<th>35802</th>
			<td>2023</td>
			<td>3</td>
			<td>31</td>
			<td>23</td>
			<td>0.0</td>
			<td>0.0</td>
			<td>996.633333</td>
			<td>74.666667</td>
			<td>14.433333</td>
			<td>63.333333</td>
			<td>3.233333</td>
		</tr>
		<tr>
			<th>35803</th>
			<td>2023</td>
			<td>4</td>
			<td>1</td>
			<td>0</td>
			<td>0.0</td>
			<td>0.0</td>
			<td>996.700000</td>
			<td>77.333333</td>
			<td>14.100000</td>
			<td>78.333333</td>
			<td>2.466667</td>
		</tr>
		<tr>
			<th>35804</th>
			<td>2023</td>
			<td>4</td>
			<td>1</td>
			<td>1</td>
			<td>0.0</td>
			<td>0.0</td>
			<td>996.900000</td>
			<td>80.333333</td>
			<td>13.866667</td>
			<td>124.000000</td>
			<td>1.500000</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>

<h2><span style="color:#2980b9">Carga datos transporte p&uacute;blico y distancia a las playas</span></h2>

<p>Tambi&eacute;n creemos que conocer cu&aacute;ntas paradas de transporte p&uacute;blico, bus o metro, quedan cerca de una estaci&oacute;n de bicing puede contribuir al modelo de predicci&oacute;n. Para ello accedemos a los datos publicados por el Ajuntament de Barcelona <a href="https://opendata-ajuntament.barcelona.cat/resources/bcn/GuiaBCN/TRANSPORTS.csv">https://opendata-ajuntament.barcelona.cat/resources/bcn/GuiaBCN/TRANSPORTS.csv</a>&nbsp;y usando la ubicaci&oacute;n de cada estaci&oacute;n (latitud y longitud) y la de las paradas de transporte, calculamos las que quedan a menos de medio kil&oacute;metro de cada estaci&oacute;n, las contamos y asignamos un n&uacute;mero entero a cada estaci&oacute;n.</p>

<p>De forma similar procedemos para calcular la dist&agrave;ncia, en metros, de cada estaci&oacute;n a las playas:<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja de Sant Sebasti&agrave;&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja de la Nova Ic&agrave;ria&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja del Somorrostro&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja de la Barceloneta&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja de la Nova Mar Bella&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja de Llevant&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja del Bogatell&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Platja de Sant Miquel&#39;,<br />
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&#39;Zona de Banys&#39;</p>

<p>Estas dos nuevas variables las a&ntilde;adimos al fichero de metadatos de las estaciones, <strong>Informacio_Estacions_Bicing.csv</strong>, para posteriormente a&ntilde;adirlo al training o a los datos a predecir si finalmente se tienen en &nbsp;cuenta, y se llamar&aacute;n <strong>n_transp_500m</strong> y&nbsp;<strong>min_dist_to_beach</strong>.&nbsp;El aspecto del dataframe cuando lo carguemos ser&aacute;:</p>

<table border="\&quot;1\&quot;">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th>station_id</th>
			<th>name</th>
			<th>lat</th>
			<th>lon</th>
			<th>altitude</th>
			<th style="width:141px">address</th>
			<th style="width:75px">post_code</th>
			<th style="width:74px">capacity</th>
			<th style="width:102px">n_transp_500m</th>
			<th>min_dist_to_beach</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>0</th>
			<td>1</td>
			<td>GRAN VIA CORTS CATALANES, 760</td>
			<td>41.397978</td>
			<td>2.180107</td>
			<td>16.0</td>
			<td style="width:141px">GRAN VIA CORTS CATALANES, 760</td>
			<td style="width:75px">8013</td>
			<td style="width:74px">46</td>
			<td style="width:102px">3.0</td>
			<td>2048.805533</td>
		</tr>
		<tr>
			<th>1</th>
			<td>2</td>
			<td>C/ ROGER DE FLOR, 126</td>
			<td>41.395488</td>
			<td>2.177198</td>
			<td>17.0</td>
			<td style="width:141px">C/ ROGER DE FLOR, 126</td>
			<td style="width:75px">8013</td>
			<td style="width:74px">29</td>
			<td style="width:102px">11.0</td>
			<td>2012.807353</td>
		</tr>
		<tr>
			<th>...</th>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td style="width:141px">...</td>
			<td style="width:75px">...</td>
			<td style="width:74px">...</td>
			<td style="width:102px">...</td>
			<td>...</td>
		</tr>
		<tr>
			<th>503</th>
			<td>518</td>
			<td>C/ LLOBREG&Oacute;S, 115</td>
			<td>41.424689</td>
			<td>2.157049</td>
			<td>112.0</td>
			<td style="width:141px">C/ LLOBREG&Oacute;S, 115</td>
			<td style="width:75px">8032</td>
			<td style="width:74px">27</td>
			<td style="width:102px">4.0</td>
			<td>5370.528992</td>
		</tr>
		<tr>
			<th>504</th>
			<td>519</td>
			<td>C/ PEDRELL, 52</td>
			<td>41.424655</td>
			<td>2.166289</td>
			<td>110.0</td>
			<td style="width:141px">C/ PEDRELL, 52</td>
			<td style="width:75px">8032</td>
			<td style="width:74px">24</td>
			<td style="width:102px">0.0</td>
			<td>4777.728819</td>
		</tr>
	</tbody>
</table>

<h2>&nbsp;</h2>

<h2><span style="color:#2980b9">Carga datos festivos y eventos</span></h2>

<p>Generamos un fichero csv con la relaci&oacute;n de dias festivos, distintos a domingo desde marzo 2019 hasta la fecha. Para el training usaremos solo hasta diciembre 2022 inclu&iacute;do, y las fechas de 2023 seran para la predicci&oacute;n. El formato de la fecha es: &nbsp;yyy-mm-dd</p>

<table border="1">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th><span style="font-size:12px">date</span></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th><span style="font-size:12px">0</span></th>
			<td><span style="font-size:12px">2019-01-01</span></td>
		</tr>
		<tr>
			<th><span style="font-size:12px">1</span></th>
			<td><span style="font-size:12px">2019-01-05</span></td>
		</tr>
		<tr>
			<th><span style="font-size:12px">2</span></th>
			<td><span style="font-size:12px">2019-04-19</span></td>
		</tr>
		<tr>
			<th><span style="font-size:12px">...</span></th>
			<td><span style="font-size:12px">...</span></td>
		</tr>
		<tr>
			<th><span style="font-size:12px">69</span></th>
			<td><span style="font-size:12px">2023-12-25</span></td>
		</tr>
		<tr>
			<th><span style="font-size:12px">70</span></th>
			<td><span style="font-size:12px">2023-12-26</span></td>
		</tr>
	</tbody>
</table>

<p>Usaremos estos datos para crear en el fichero de training una variable 0/1 llamada holiday<br />
&nbsp;</p>

<h2><span style="color:#2980b9">Carga datos adicionales</span></h2>

<p>Adem&aacute;s de los datos mencionados anteriormente, creemos interesante a&ntilde;adir algunas variables m&aacute;s al dataset de training:</p>

<h3><span style="color:#2980b9">Metadatos de las estaciones</span></h3>

<p>Incorporaremos las siguientes variables de los metadatos de las estaciones:</p>

<ul>
	<li><strong>altitude</strong></li>
	<li><strong>capacity</strong></li>
	<li><strong>post_code</strong></li>
</ul>

<h3><span style="color:#2980b9">Variables obtenidas a partir de los datos iniciales del dataset de training&nbsp;</span></h3>

<p>Del an&aacute;lisis hecho de los datos &nbsp;concluimos que las siguientes variables, calculadas a partir de las fechas , se deber&iacute;an incluir:</p>

<ul>
	<li><strong>weekend</strong>: 1 si el dia de la semana es s&aacute;bado o domingo; 0 en caso contrario</li>
	<li><strong>peekhour</strong>: &nbsp;1 si &nbsp;laborable y la hora est&aacute; entre 8 y 10 &oacute; entre 17 y 19; 0 en caso contrario</li>
	<li><strong>holiday</strong>: 1 si festivo distinto de domingo; 0 en caso contrario</li>
	<li><strong>season</strong>: estaci&oacute;n del a&ntilde;o -&gt; 1 invierno; 2 primavera u oto&ntilde;o; 3 verano,</li>
</ul>

<h3><span style="color:#2980b9">Zonas de estaciones de bicicletas</span></h3>

<p>Como usuarios del bicing y tambi&eacute;n analizando los datos hemos visto que ciertas estaciones parecen tener &nbsp;un comportamiento similar a lo largo del tiempo. Tenemos problemas computacionales si aplicamos OneHotEncoder a variables con muchos valores, por ejemplo a station_id &nbsp;(505 opciones), por lo que decidimos agrupar las estaciones en cinco tipos. La variable se llamar&aacute; <strong>zone</strong>&nbsp;y los valores posibles son:</p>

<ul>
	<li><strong>bicing_platges</strong>: todas las estaciones cerca de la playa</li>
	<li><strong>bicing_pcatalunya</strong>: todas las estaciones del centro y alrededor incluyendo universidad de Barcelona, plaza Urquinaona..centro</li>
	<li><strong>bicing_uni</strong>: las estaciones alreadedor de la zona universitaria diagonal</li>
	<li><strong>bicing_alta</strong>: las estaciones que se encuentra a m&aacute;s de 60 metros del nivel del mar (subir cuesta arriba puede ser un inconveniente a usar el bicing)</li>
	<li><strong>bicing_other</strong>: el resto de estaciones</li>
</ul>

<p>&nbsp;</p>

<p>Finalmente cargamos nuestro dataframe de training inicial con todas las variables mencionadas anteriormente. Para ellos crearemos un pipeline, add_features, &nbsp;para poder a&ntilde;adir estas variables &nbsp;tambi&eacute;n al conjunto de test o validaci&oacute;n, y a las futuras predicciones que queramos hacer. Si finalmente alguna de las variables mencionadas anteriormente no se incluyera en el modelo, corregir&iacute;amos el pipeline. El aspecto que tendr&aacute; nuestro dataframe de training ahora ser&aacute;:</p>

<table border="1">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th>station_id</th>
			<th>year</th>
			<th>month</th>
			<th>day</th>
			<th>hour</th>
			<th>capacity</th>
			<th>altitude</th>
			<th>percentage_docks_available</th>
			<th>ctx-4</th>
			<th>ctx-3</th>
			<th>...</th>
			<th>holiday</th>
			<th>season</th>
			<th>zone</th>
			<th>RS</th>
			<th>PPT</th>
			<th>P</th>
			<th>HR</th>
			<th>T</th>
			<th>DV10</th>
			<th>VV10</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>0</th>
			<td>1</td>
			<td>2019</td>
			<td>3</td>
			<td>28</td>
			<td>22</td>
			<td>46.0</td>
			<td>16.0</td>
			<td>0.021739</td>
			<td>0.304348</td>
			<td>0.280435</td>
			<td>...</td>
			<td>0</td>
			<td>1</td>
			<td>other</td>
			<td>0.000000</td>
			<td>0.0</td>
			<td>1007.433333</td>
			<td>65.666667</td>
			<td>11.433333</td>
			<td>283.666667</td>
			<td>1.766667</td>
		</tr>
		<tr>
			<th>1</th>
			<td>1</td>
			<td>2019</td>
			<td>3</td>
			<td>29</td>
			<td>3</td>
			<td>46.0</td>
			<td>16.0</td>
			<td>0.000000</td>
			<td>0.009058</td>
			<td>0.003623</td>
			<td>...</td>
			<td>0</td>
			<td>1</td>
			<td>other</td>
			<td>0.000000</td>
			<td>0.0</td>
			<td>1006.266667</td>
			<td>47.333333</td>
			<td>10.800000</td>
			<td>307.666667</td>
			<td>2.866667</td>
		</tr>
		<tr>
			<th>2</th>
			<td>1</td>
			<td>2019</td>
			<td>3</td>
			<td>29</td>
			<td>8</td>
			<td>46.0</td>
			<td>16.0</td>
			<td>0.432971</td>
			<td>0.009058</td>
			<td>0.007246</td>
			<td>...</td>
			<td>0</td>
			<td>1</td>
			<td>other</td>
			<td>247.333333</td>
			<td>0.0</td>
			<td>1007.366667</td>
			<td>53.666667</td>
			<td>11.900000</td>
			<td>118.000000</td>
			<td>1.733333</td>
		</tr>
		<tr>
			<th>...</th>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
		</tr>
		<tr>
			<th>2972603</th>
			<td>519</td>
			<td>2022</td>
			<td>12</td>
			<td>31</td>
			<td>13</td>
			<td>24.0</td>
			<td>110.0</td>
			<td>1.000000</td>
			<td>0.871528</td>
			<td>0.902778</td>
			<td>...</td>
			<td>0</td>
			<td>4</td>
			<td>alta</td>
			<td>430.333333</td>
			<td>0.0</td>
			<td>1003.866667</td>
			<td>37.000000</td>
			<td>20.700000</td>
			<td>259.000000</td>
			<td>2.633333</td>
		</tr>
		<tr>
			<th>2972604</th>
			<td>519</td>
			<td>2022</td>
			<td>12</td>
			<td>31</td>
			<td>18</td>
			<td>24.0</td>
			<td>110.0</td>
			<td>0.906250</td>
			<td>0.965278</td>
			<td>0.944444</td>
			<td>...</td>
			<td>0</td>
			<td>4</td>
			<td>alta</td>
			<td>0.000000</td>
			<td>0.0</td>
			<td>1004.066667</td>
			<td>72.000000</td>
			<td>15.300000</td>
			<td>244.666667</td>
			<td>2.033333</td>
		</tr>
		<tr>
			<th>2972605</th>
			<td>519</td>
			<td>2022</td>
			<td>12</td>
			<td>31</td>
			<td>23</td>
			<td>24.0</td>
			<td>110.0</td>
			<td>0.583333</td>
			<td>0.885417</td>
			<td>0.760417</td>
			<td>...</td>
			<td>0</td>
			<td>4</td>
			<td>alta</td>
			<td>0.000000</td>
			<td>0.0</td>
			<td>1005.466667</td>
			<td>73.333333</td>
			<td>13.633333</td>
			<td>111.000000</td>
			<td>1.966667</td>
		</tr>
	</tbody>
</table>

<p>Comprobamos si tenemos valores nulos, y encontramos que dos variables s&iacute;. Veremos m&aacute;s adelante c&oacute;mo lo tratamos.</p>

<p>Out[52]:</p>

<pre>
Index([&#39;n_transp_500m&#39;, &#39;min_dist_to_beach&#39;], dtype=&#39;object&#39;)</pre>

<h1>&nbsp;</h1>

<h1><span style="color:#2980b9"><strong>Visualizaci&oacute;n de los datos</strong></span></h1>

<p>Como las incorporaciones que hemos hecho, vamos a ver ahora qu&eacute; forma tienen todos nuestros datos y correlaci&oacute;n entre ellos</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_histogramas.png" style="height:670px; width:900px" /></p>

<ul>
	<li>Vemos que de algunas estaciones hay menos registros, pero es correcto pues algunas estaciones de 2023 se activaron en 2020, 2021 e incluso algunas en 2022</li>
	<li>Tenemos menos registros en 2019 y 2020 que en 2021 y 2022 donde los registrados son muy similares. La raz&oacute;n, el registro de esta informaci&oacute;n p&uacute;blica se inicia a finales de marzo de 2019 (casi tres meses menos de registros) y en 2020 debido a la pandemia el servicio tambi&eacute;n estuvo unas semanas desactivado. Cuando miramos los datos por mesos, apreciamos tambi&eacute;n esas diferencias.</li>
	<li>Si analizamos por dias del mes, tenemos n&uacute;meros de registros bastante similares.</li>
	<li>Por horas el n&uacute;mero de registros es pr&aacute;cticamente igual, eso nos va muy bien para entrenar el modelo</li>
	<li>Ampliamos PPT&nbsp;</li>
</ul>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_PPT.png" style="height:111px; margin-left:50px; margin-right:50px; width:150px" /></p>

<ul>
	<li>Las variables <strong>altitute</strong>, <strong>PPT</strong>, <strong>RS</strong> tienen cola alargada hacia la derecha, aplicaremos una transformaci&oacute;n logaritmica antes de estandarizar.</li>
</ul>

<h3>&nbsp;</h3>

<h3><span style="color:#2980b9"><strong>Outliers</strong></span></h3>

<p>Pasamos a analizar con m&aacute;s detalle las variable meteorol&oacute;gicas, min_dist_to_beach, n_transp_500m y la variable target percentange_docks_available</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_WeatherOutliers.png" style="height:445px; width:800px" /></p>

<p>La <strong>temperatura(T)</strong> y <strong>direcci&oacute;n del viento(DV10)</strong> no tienen outliers, el resto s&iacute;. &nbsp;Analizamos con m&aacute;s detalle las variables&nbsp;<strong>PPT </strong>(precipitaci&oacute;n)<strong> </strong>y<strong> VV10 </strong>(velocidad del viento)</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_PPT_VV10_Outliers.png" style="height:335px; width:600px" /></p>

<p>La precipitaci&oacute;n ha sido tan escasa en el per&iacute;odo considerado (especialmente seco) que los registros con lluvia de por s&iacute; ya son outliers. No aplicaremos la transformaci&oacute;n basada en los quantiles en estes caso, y estandarizaremos la variable para mitigar el impacto de esos valores tan dispares, pero como veremos m&aacute;s adelante, &eacute;sta es una variable que finalmente no se incluir&aacute; en el modelo.</p>

<p>Por otra parte, <strong>min_dist_to_beach</strong> no tiene outliers, y <strong>n_transp_500m</strong> algunos que tambi&eacute;n trataremos</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_distbeachOutliers.png" style="height:269px; width:500px" /><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_numPTOutliers.png" style="height:273px; width:500px" /></p>

<p>La variable target, como vemos debajo, no tiene outiers, y las variables ctx-4, ctx-3, ctx-2, y ctx-1 obtenidas a partir de la variable target tampoco, como era de esperar</p>

<p>&nbsp;</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_labelOutliers.png" style="height:225px; width:400px" /><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_ctxOutliers.png" style="height:217px; width:400px" /></p>

<p>&nbsp;</p>

<h3><span style="color:#2980b9"><strong>Transformaciones</strong></span></h3>

<p>Despu&eacute;s de analizar las gr&aacute;ficas nos planteamos las siguientes transformaciones, donde &nbsp;<strong>Replace_Outliers_2_NaN </strong>es una funci&oacute;n que calcula los l&iacute;mites superiore e inferior a partir de los quantiles 75% y 25% y todos los valores por encima o por debajo se redefinen como NaN.</p>

<p>Todos los NaN de cada variable se reemplazar&aacute;n por el valor de la mediana de dicha variable. Todas las variables num&eacute;ricas ser&aacute;n tambi&eacute;n estandarizadas</p>

<p style="margin-left:40px"><span style="color:#2980b9">variables num&eacute;ricas</span></p>

<p style="margin-left:40px">num1_attribs=[&#39;<strong>altitude</strong>&#39;,&#39;<strong>PPT</strong>&#39;]<br />
num1_pipeline = Pipeline([<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;imputer&#39;, <strong>SimpleImputer</strong>(strategy=&quot;median&quot;)),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;log&#39;,FunctionTransforme<strong>r</strong>(<strong>np.log1p</strong>)),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;std_scaler&#39;, <strong>StandardScaler</strong>()),<br />
&nbsp; &nbsp; ])</p>

<p style="margin-left:40px">num2_attribs = [&#39;<strong>capacity</strong>&#39;,&#39;<strong>T</strong>&#39;,&#39;<strong>min_dist_to_beach</strong>&#39;] &nbsp;<br />
num2_pipeline = Pipeline([<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;imputer&#39;, <strong>SimpleImputer</strong>(strategy=&quot;median&quot;)),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;std_scaler&#39;, <strong>StandardScaler</strong>()),<br />
&nbsp; &nbsp; ])</p>

<p style="margin-left:40px">num3_attribs=[&#39;ctx-4&#39;,&#39;ctx-3&#39;,&#39;ctx-2&#39;,&#39;ctx-1&#39;,&#39;weekend&#39;,&#39;peekhour&#39;,&#39;holiday&#39;] #passthrough</p>

<p style="margin-left:40px">num4_attribs=[&#39;<strong>n_transp_500m</strong>&#39;,&#39;<strong>HR</strong>&#39;,&#39;<strong>VV10</strong>&#39;,&#39;<strong>P</strong>&#39;,&#39;<strong>RS</strong>&#39;]<br />
num4_pipeline = Pipeline([<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;replace_outliers&#39;,<strong>Replace_Outliers_2_NaN</strong>()),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;imputer&#39;, <strong>SimpleImputer</strong>(strategy=&quot;median&quot;)),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;std_scaler&#39;, <strong>StandardScaler</strong>()),<br />
&nbsp; &nbsp; ])</p>

<p style="margin-left:40px"><span style="color:#2980b9">variabales que pasan a ser tratadas como categ&oacute;ricas</span></p>

<p style="margin-left:40px">cat1_attribs = [&#39;<strong>station_id</strong>&#39;,&#39;<strong>post_code</strong>&#39;,&#39;<strong>year</strong>&#39;,&#39;<strong>month</strong>&#39;,&#39;<strong>hour</strong>&#39;,&#39;<strong>season</strong>&#39;]<br />
cat1_pipeline = Pipeline([<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;transform_to_Cat&#39;,FunctionTransformer(func = <strong>transform_Num_to_Cat</strong>,validate=False)),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;imputer&#39;, <strong>SimpleImputer</strong>(strategy=&quot;constant&quot;,fill_value=&#39;Unknown&#39;)),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&#39;ordinal_encoder&#39;, <strong>OrdinalEncoder</strong>()),<br />
&nbsp; &nbsp; ])<br />
cat2_attribs=[&#39;<strong>zone</strong>&#39;] #ja era categ&ograve;rica<br />
cat2_pipeline = Pipeline([<br />
&nbsp; &nbsp; (&#39;imputer&#39;, <strong>SimpleImputer</strong>(strategy=&quot;constant&quot;,fill_value=&#39;Unknown&#39;)), &nbsp;<br />
&nbsp; &nbsp; (&#39;one_hot_encoder&#39;, <strong>OneHotEncoder</strong>(handle_unknown=&#39;ignore&#39;)),<br />
&nbsp; &nbsp; ])</p>

<p style="margin-left:40px"><span style="color:#2980b9">unimos todas las transformaciones</span></p>

<p style="margin-left:40px">full_pipeline = ColumnTransformer([<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&quot;num1&quot;, num1_pipeline, num1_attribs),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&quot;num2&quot;, num2_pipeline, num2_attribs),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&quot;cat1&quot;, cat1_pipeline, cat1_attribs),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&quot;cat2&quot;, cat2_pipeline, cat2_attribs),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&quot;num3&quot;, &#39;passthrough&#39;, num3_attribs),<br />
&nbsp; &nbsp; &nbsp; &nbsp; (&quot;num4&quot;, num4_pipeline, num4_attribs),<br />
&nbsp; &nbsp; &nbsp; &nbsp; ])</p>

<p style="margin-left:40px">&nbsp;</p>

<h3><span style="color:#2980b9"><strong>Correlaci&oacute;n entre las distintas variables y percentage_docks_avaialble</strong></span></h3>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura6_corrmatrix.png" style="height:693px; width:900px" /></p>

<p>Las variables <strong>ctx-4</strong>, <strong>ctx-3</strong>, <strong>ctx-2</strong> y <strong>ctx-1</strong> est&aacute;n fuertemente correlacionadas con la variable target, percentage_docks_available, como era de esperar por la manera en que se han calculado.</p>

<p>La variable del tiempo <strong>RS</strong> (Irradiancia solar global) est&aacute; bastante correlacionada con <strong>HR</strong>(humedat relativa) y con <strong>T</strong>(temperatura). Nos planteamos prescindir de RS.</p>

<p>Como punto de partida prescindiremos de la variable <strong>DV10</strong>(direcci&oacute;n del viento).</p>

<p><strong>altitude</strong> y <strong>min_dist_to_beach</strong> tienen correlaci&oacute;n con la variable target, y aunque entre ellas est&aacute;n fuertemente correlacionadas puesto que las estacioneos en la playa tienen altitud cero o casi, su significado es bien distinto pq el uso de las estaciones de bicicletas de la zona de playa no viene influenciado directametne por la altura (nivel del mar) a la que estan sin&oacute; por encontrarse en un sitio de mucho inter&eacute;s en el tiempo libre.</p>

<p>&nbsp;</p>

<h1><span style="color:#2980b9"><strong>Modelo: selecci&oacute;n, entrenamiento, scores</strong></span></h1>

<h3><span style="color:#2980b9"><strong>Estratificaci&oacute;n, split train - test&nbsp;</strong></span></h3>

<p>Es momento de proceder a dividir el dataset entre la parte que usaremos para el entrenamiento y la parte que reservaremos para validar el modelo (test). Para asegurarnos que ambos sets mantienen la misma proporci&oacute;n de tipos de datos, evaluamos varias formas de estratificar los datos:</p>

<ul>
	<li>Opci&oacute;n 1&nbsp;&nbsp;[&#39;<strong>station_id</strong>&#39;,&#39;<strong>month</strong>&#39;,&#39;<strong>hour</strong>&#39;,&#39;<strong>day</strong>&#39;] : no funciona (obtenemos el error&nbsp;ValueError: The least populated class in y has only&nbsp;1 member, which is too few. The minimum number of groups for any class cannot be less than 2.)</li>
	<li>Opci&oacute;n 2&nbsp;[&#39;<strong>year</strong>&#39;,&#39;<strong>month</strong>&#39;,&#39;<strong>hour</strong>&#39;,&#39;<strong>day</strong>&#39;] : realizamos un primer entrenamientos con una simple regresi&oacute;n lineal&nbsp;y vemos que nos ayuda a hacer una mejor predicci&oacute;n, con menos error MSE</li>
	<li>Opci&oacute;n 3 [&#39;<strong>month</strong>&#39;,&#39;<strong>hour</strong>&#39;,&#39;<strong>day</strong>&#39;] : mejores resultados que si no estratificamos, pero no mejora la opci&oacute;n anterior</li>
	<li>Opci&oacute;n 4 [&#39;<strong>disponibilitat</strong>&#39;] : creamos una variable categ&oacute;rica a partir de la variable target, percentage_docks_available, que nos clasifica cada estaci&oacute;n en 5 categor&iacute;as posibles seg&uacute;n el nivel de disponibilidad de docks:</li>
</ul>

<p style="margin-left:80px"><span style="font-size:11px">&nbsp;Out[43]:</span></p>

<pre style="margin-left:80px">
<span style="font-size:11px">[&#39;for&ccedil;a ple&#39;, &#39;ple&#39;, &#39;mig buit&#39;, &#39;quasi buit&#39;, &#39;buit&#39;]
Categories (5, object): [&#39;ple&#39; &lt; &#39;for&ccedil;a ple&#39; &lt; &#39;mig buit&#39; &lt; &#39;quasi buit&#39; &lt; &#39;buit&#39;]</span>
</pre>

<p>Procedemos a estratificar seg&uacute;n opci&oacute;n 4 y a continuaci&oacute;n eliminamos las variables target y la categ&oacute;rica disponibilitat usada para estratificar, pues no deben incluirse como variables de entrenamiento,. Tambi&eacute;n comprobamos shape de ambos datasets :</p>

<p style="margin-left:40px"><span style="font-size:11px">In&nbsp;[55]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">labels=bicing[&#39;percentage_docks_available&#39;].copy()</span></pre>

<p style="margin-left:40px"><span style="font-size:11px">In&nbsp;[56]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">labels.isna().any()</span></pre>

<p style="margin-left:40px"><span style="font-size:11px">Out[56]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">False</span></pre>

<p style="margin-left:40px"><span style="font-size:11px">In&nbsp;[57]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">X_train, X_test, y_train, y_test = train_test_split(bicing,labels,test_size=.2,random_state=seed,shuffle=True,stratify=bicing[&#39;disponibilitat&#39;])</span></pre>

<p style="margin-left:40px"><span style="font-size:11px">In&nbsp;[58]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">for set_ in (X_train, X_test):</span></pre>

<pre style="margin-left:40px">
<span style="font-size:11px">    set_.drop(columns=[&#39;percentage_docks_available&#39;,&#39;disponibilitat&#39;],inplace=True)</span></pre>

<p style="margin-left:40px"><span style="font-size:11px">In&nbsp;[59]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">Training Shape: X (2378084, 26) , y: (2378084,)
Testing Shape: X (594522, 26) , y: (594522,)</span></pre>

<p>El dataset de entrenamiento, <strong>X_train</strong>, tiene este aspecto:</p>

<table border="1">
	<thead>
		<tr>
			<th>&nbsp;</th>
			<th>station_id</th>
			<th>year</th>
			<th>month</th>
			<th>day</th>
			<th>hour</th>
			<th>capacity</th>
			<th>altitude</th>
			<th>ctx-4</th>
			<th>ctx-3</th>
			<th>ctx-2</th>
			<th>...</th>
			<th>holiday</th>
			<th>season</th>
			<th>zone</th>
			<th>RS</th>
			<th>PPT</th>
			<th>P</th>
			<th>HR</th>
			<th>T</th>
			<th>DV10</th>
			<th>VV10</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th>1307303</th>
			<td>221</td>
			<td>2022</td>
			<td>11</td>
			<td>7</td>
			<td>17</td>
			<td>24.0</td>
			<td>68.0</td>
			<td>0.881410</td>
			<td>0.906250</td>
			<td>0.850694</td>
			<td>...</td>
			<td>0</td>
			<td>4</td>
			<td>other</td>
			<td>23.666667</td>
			<td>0.000000</td>
			<td>997.766667</td>
			<td>75.666667</td>
			<td>17.566667</td>
			<td>231.000000</td>
			<td>2.300000</td>
		</tr>
		<tr>
			<th>126916</th>
			<td>22</td>
			<td>2021</td>
			<td>8</td>
			<td>22</td>
			<td>15</td>
			<td>19.0</td>
			<td>28.0</td>
			<td>0.732456</td>
			<td>0.832536</td>
			<td>0.688596</td>
			<td>...</td>
			<td>0</td>
			<td>3</td>
			<td>other</td>
			<td>689.333333</td>
			<td>0.000000</td>
			<td>1000.266667</td>
			<td>65.333333</td>
			<td>28.233333</td>
			<td>159.666667</td>
			<td>3.000000</td>
		</tr>
		<tr>
			<th>...</th>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
			<td>...</td>
		</tr>
		<tr>
			<th>155335</th>
			<td>27</td>
			<td>2019</td>
			<td>10</td>
			<td>2</td>
			<td>21</td>
			<td>21.0</td>
			<td>38.0</td>
			<td>0.869048</td>
			<td>0.892857</td>
			<td>0.944444</td>
			<td>...</td>
			<td>0</td>
			<td>4</td>
			<td>other</td>
			<td>0.000000</td>
			<td>0.000000</td>
			<td>994.200000</td>
			<td>68.000000</td>
			<td>20.133333</td>
			<td>109.000000</td>
			<td>2.033333</td>
		</tr>
		<tr>
			<th>1912954</th>
			<td>319</td>
			<td>2020</td>
			<td>1</td>
			<td>20</td>
			<td>13</td>
			<td>31.0</td>
			<td>51.0</td>
			<td>0.271505</td>
			<td>0.352151</td>
			<td>0.403226</td>
			<td>...</td>
			<td>0</td>
			<td>1</td>
			<td>other</td>
			<td>135.333333</td>
			<td>0.000000</td>
			<td>1004.133333</td>
			<td>57.000000</td>
			<td>8.566667</td>
			<td>60.333333</td>
			<td>9.866667</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>

<h3><span style="color:#2980b9"><strong>Column Transformers</strong></span></h3>

<p>Procedemos a aplicar las transformaciones comentadas en la secci&oacute;n anterior: fit &amp; transform al set de entrenamiento , y s&oacute;lo transform al set de validaci&oacute;n. Comprobamos que mantenemos las mismas dimensiones de los sets:</p>

<p style="margin-left:40px">train_prepared = full_pipeline.<strong>fit_transform</strong>(X_train)</p>

<p style="margin-left:40px"><span style="font-size:11px">Out[186]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">array([[ 1.12779005, -0.12501115, -0.47456499, ..., -0.02281921,
         0.21363936, -0.33404425],
       [ 0.2531122 , -0.12501115, -1.25540877, ..., -0.09947645,
        -0.02402338, -0.49281287],
       [-0.28581762,  0.45802176, -0.94307126, ..., -0.09947645,
        -0.02402338, -0.49281287],
       ...,
       [ 0.91714057, -0.12501115, -0.47456499, ..., -0.09947645,
        -0.02402338, -0.49281287],
       [ 0.55206692, -0.12501115, -0.94307126, ..., -0.32944819,
        -0.69457182, -0.49281287],
       [ 0.84236   , -0.12501115,  0.61861632, ..., -0.09947645,
        -0.02402338, -0.49281287]])</span>
</pre>

<p style="margin-left:40px">train_prepared.shape</p>

<p style="margin-left:40px"><span style="font-size:11px">Out[187]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">(2378084, 28) <span style="color:#e74c3c">(revisar si he adjuntat la versi&oacute; final)</span></span></pre>

<p style="margin-left:40px">test_prepared = full_pipeline.<strong>transform</strong>(X_test)</p>

<p style="margin-left:40px"><span style="font-size:11px">Out[188]:</span></p>

<pre style="margin-left:40px">
<span style="font-size:11px">(594522, 28) <span style="color:#e74c3c">(revisar si he adjuntat la versi&oacute; final)</span></span></pre>

<h3>&nbsp;</h3>

<h3><span style="color:#2980b9"><strong>Entrenamiento</strong></span></h3>

<p>Hacemos un primer entrenamiento con los siguientes modelos:</p>

<ul>
	<li>Linea Regression</li>
	<li>KNeighborsRegressor</li>
	<li>RandomForestRegressor</li>
	<li>GradientBoostingRegressor</li>
</ul>

<p>El estad&iacute;stico que usaremos para comparar el funcionamento de cada modelo es Mean Square Error. Parece que los mejores modelos son Random Forest Regressor y Gradient Boosting Regressor, pero procedemos a realizar un cross_validation con 10 folks, para valorar el funcionamiento en promedio seg&uacute;n va variando la parte sobre la que se hace el &nbsp;training. Los resultados obtenidos son:</p>

<p>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;<img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura7_cross_validation_cv10.png" style="height:129px; width:250px" /></p>

<h1>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura7_modelscomparison.png" style="height:397px; width:800px" /></h1>

<h3><span style="color:#2980b9"><strong>B&uacute;squeda de los mejores par&aacute;metros</strong></span></h3>

<p>Por ahora parece que el mejor modelo es Random Forest Regressor. Procedemos a hacer una b&uacute;squeda para encontrar los mejore &nbsp;hiperpar&aacute;metros. Tambi&eacute;n en este caso aplicaremos k-fold (pero m&aacute;s peque&ntilde;o pues nos enfrentamos a &nbsp;limitaciones computacionales de nuestros laptops).</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura8_hyperparametersRF.png" style="height:228px; width:700px" /></p>

<h1><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura8_bestRF_Model.png" style="height:126px; width:600px" /></h1>

<p><strong><span style="color:#2980b9">Best Score:</span></strong></p>

<pre>
<span style="font-size:11px">0.10099171959343188</span>
</pre>

<p><span style="color:#2980b9"><strong>Predicci&oacute;n set de validaci&oacute;n</strong></span></p>

<p>Obtenemos las predicciones de los set de validaci&oacute;n con el modelo seleccionado y calculamos MSE, y tambi&eacute;n R2</p>

<pre>
<span style="font-size:11px">MSE (train | test):
1.7116009007665552e-31 0.010009291226164419
R2 (train | test):
0.98 0.8547846062511928</span>
</pre>

<h1><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura8_bestRF_Features.png" style="height:450px; width:600px" /></h1>

<p>Dado que no hab&iacute;a mucha diferencia entres los estimadores Random Forest Regresso y <strong>Grandient Boosting Regressor</strong>, exploramos de nuevo el segundo estimador, para ver si mejoramos resultados.&nbsp;Conseguimos el mejor resultado con los par&aacute;metros:</p>

<p><strong><span style="color:#2980b9">Best Score:</span></strong></p>

<pre>
<span style="font-size:11px">0.10099171959343188</span></pre>

<p><span style="color:#2980b9"><strong>Predicci&oacute;n set de validaci&oacute;n</strong></span></p>

<p>MSE (train | test):<br />
0.009707910879462097 0.009752140802141927<br />
R2 (train | test):<br />
0.8641781895663517 0.863633803236243</p>

<p><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura8_bestGB_Features.png" style="height:450px; width:600px" /></p>

<p>Como podemos ver, el peso de los par&aacute;metros es muy distinto a los obtenido con el estimador Random Forest Regressor.</p>

<p>Por &uacute;ltimo, exploramos el estimador <strong>XGBoost, </strong>que es el que nos funciona mejor</p>

<p>xgb_model = xgb.XGBRegressor(n_estimators=1000,)</p>

<p>&nbsp;</p>

<pre>
<img src="https://ckeditor.com/apps/ckfinder/userfiles/files/figura8_XGB_performance.png" style="height:413px; width:556px" />

<span style="color:#2980b9"><strong>Predicci&oacute;n set de validaci&oacute;n
</strong></span>MSE (train | test):
0.008935940587087248 0.009439234663387547
R2 (train | test):
0.8761112236824559 0.8690996304193535</pre>

<p>&nbsp;</p>

<h2><span style="color:#2980b9"><strong>Explicaci&oacute;n del modelo seleccionado: </strong></span></h2>

<h2>XGBoost(n_estimators=1000,&nbsp;early_stopping_rounds=10, eta=0.1)</h2>

<h1><img src="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura8_bestXGB_Features.png" style="height:574px; width:600px" /></h1>

<h1>&nbsp;</h1>

<h1><span style="color:#2980b9"><strong>Desplegamiento del modelo (streamlit)</strong></span></h1>

<p>&nbsp;</p>

<p>&nbsp;</p>

<p>&nbsp;</p>

<p><a href="https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura1_2020.png">https://raw.githubusercontent.com/olgallima/olgallima.github.io/main/figura1_2020.png</a></p>

<p>&nbsp;</p>

<p>&nbsp;</p>

<p>&nbsp;</p>


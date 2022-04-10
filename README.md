# MagicMirror² Module: YrThen

<img src="/images/newShot.png" align="right"/>This is an unofficial Yr Weather Forecast module for [MagicMirror²](https://github.com/MichMich/MagicMirror), which displays data from [Yr](https://www.yr.no/nb/).

It is heavily based on [MMM-YrNow](https://github.com/YR/MMM-YrNow), from Yr itself. Yr is a weather service from the Norwegian Broadcasting Corporation and the Norwegian Meteorological Institute.

This is work in progress, but as it stands right now it's working and covering my needs.

## How to install

Remote into your Magic Mirror box using a terminal software and go to the modules folder:

    cd ~/MagicMirror/modules

Clone the repository:

	git clone https://github.com/fmandal/MMM-YrThen

Install dependencies:

        cd MMM-YrThen
        npm install request --save

Add the module to the modules array in the config/config.js file by adding the following section. You can change this configuration later when you see this works:

	{
		module: 'MMM-YrThen',
		position: 'top_right',
		config: {
			location: '1-2820936',
		}
	},

Find your location using the search form at <a href="https://www.yr.no/nb/liste/dag/1-2820936/Norge/Nord-Trøndelag/Steinkjer/Skrubblivegen">this Yr.no page</a> and look for the ID in the URL.

## Configuration options

<table style="width:100%">
	<tr>
		<th>Option</th>
		<th>Comment</th>
		<th>Default</th>
	</tr>
	<tr>
		<td>location</td>
		<td>The unique Id found in the Url of any location on <a href="https://www.yr.no/nb/liste/dag/1-2820936/Norge/Nord-Trøndelag/Steinkjer/Skrubblivegen">Yr.no</a>. Default location is Skrubblivegen in Steinkjer, Norway. (String)</td>
		<td>"1-2296935"</td>
	</tr>
	<tr>
		<td>updateInterval</td>
		<td>How often to get new data. Defaults to 1 hour, as the weather forecast doesn't really change too often. (Integer)</td>
		<td>3600000</td>
	</tr>
	<tr>
		<td>initialLoadDelay</td>
		<td>Dunno why, but thought it was a good idea to give it some rest before we start. Defaults to 1 sec. (Integer)</td>
		<td>1000</td>
	</tr>
  <tr>
		<td>numDays</td>
		<td>Number of days to show if showAll is true, number of forecasts to show if showAll is false. (Integer)</td>
		<td>7</td>
	</tr>
	<tr>
		<td>showAll</td>
		<td>Show all four periods of each day or not. (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>details</td>
		<td>If showAll is false, show detailed weather forecast? If false, it only shows the forecast around midday (12.00). If true, it shows detailed forecast numDetails times. (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>showPrecipitation</td>
		<td>If showAll is true, show precipitation as well? (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>detailedPrec</td>
		<td>Show detailed precipitation? (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>showMaxMin</td>
		<td>If showAll is true, show maximum and minimum temperature? (Boolean)</td>
		<td>false</td>
	</tr>
	<tr>
		<td>maxMinSeparator</td>
		<td>If showMaxMin is true, which separator should be used? (String)</td>
		<td>"-"</td>
	</tr>
	<tr>
		<td>numDetails</td>
		<td>How many detailed forecasts to show. Default is next two periods. Only applies if showAll is false and details is true. (Integer)</td>
		<td>2</td>
	</tr>
	<tr>
		<td>roundTemp</td>
		<td>Round temperature to zero decimals. (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>roundPrec</td>
		<td>Round precipitation to zero decimals. (Boolean)</td>
		<td>false</td>
	</tr>
	<tr>
		<td>title</td>
		<td>Content of the header of the module – the title. If shown, that is. (String)</td>
		<td>"Værmelding for Skrubblivegen"</td>
	</tr>
	<tr>
		<td>header</td>
		<td>Show header or not. Contents of header is title. (Boolean)</td>
		<td>false</td>
	</tr>
	<tr>
		<td>size</td>
		<td>The size of the text. One of the CSS classes defined in main.css of MagicMirror2: "xsmall", "small", "medium", "large", "xlarge". (String)</td>
		<td>"small"</td>
	</tr>
	<tr>
		<td>windShow</td>
		<td>Show wind forecast or not? (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>windGust</td>
		<td>Show wind gust information or not. (Boolean)</td>
		<td>false</td>
	</tr>
	<tr>
		<td>windUnit</td>
		<td>If set, it shows as the unit of the wind. Default could be "m/s", but I like it at nothing at all. (string)</td>
		<td>""</td>
	</tr>
	<tr>
		<td>windSize</td>
		<td>Size of wind forecast. One of the CSS classes defined in main.css of MagicMirror2: "xsmall", "small", "medium", "large", "xlarge" – or the custom "yrthen-xxsmall" for extra, extra small. (String)</td>
		<td>"yrthen-xxsmall"</td>
	</tr>
	<tr>
		<td>windText</td>
		<td>Show wind speed in text. (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>windTextNumber</td>
		<td>Show wind speed in number after showing it in text. (Boolean)</td>
		<td>true</td>
	</tr>
	<tr>
		<td>windTextNewLine</td>
		<td>If windText and windTextNumber both are true, show windTextNumber on a new line? (Boolean)</td>
		<td>true</td>
	</tr>
</table>

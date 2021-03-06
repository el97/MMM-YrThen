# MagicMirror² Module: YrThen

<img src="/images/MMM-YrThen-screenshot.png" align="right"/>This is an unofficial Yr Weather Forecast module for [MagicMirror²](https://github.com/MichMich/MagicMirror), which displays data from [Yr](https://www.yr.no/nb/).

It is heavily based on [MMM-YrNow](https://github.com/YR/MMM-YrNow), from Yr itself. Yr is a weather service from the Norwegian Broadcasting Corporation and the Norwegian Meteorological Institute.

This is work in progress, but as it stands right now it's working and covering my needs.

## How to install

Remote into your Magic Mirror box using a terminal software and go to the modules folder:

    cd ~/MagicMirror/modules

Clone the repository:

	git clone https://github.com/fmandal/MMM-YrThen

Add the module to the modules array in the config/config.js file by adding the following section. You can change this configuration later when you see this works:

	{
		module: 'MMM-YrThen',
		position: 'top_right',
		config: {
			location: '1-2296935',
		}
	},

## Configuration options

<table style="width:100%">
	<tr>
		<th>Option</th>
		<th>Comment</th>
		<th>Default</th>
	</tr>
	<tr>
		<td>location</td>
		<td>The unique Id found in the Url of any location on <a href="https://www.yr.no/nb/liste/dag/1-2296935/Norge/Nord-Trøndelag/Steinkjer/Steinkjer">Yr</a> I.e. Steinkjer.</td>
		<td>1-2296935</td>
	</tr>
	<tr>
		<td>updateInterval</td>
		<td>How often to get new data. Defaults to 1 hour, as the weather forecast doesn't really change too often.</td>
		<td>3600000</td>
	</tr>
	<tr>
		<td>initialLoadDelay</td>
		<td>Dunno why, but thought it was a good idea to give it some rest before we start. Defaults to 1 sec.</td>
		<td>1000</td>
	</tr>
	<tr>
		<td>details</td>
		<td>Show detailed weather forecast. If false, it only shows the forecast around midday (12.00). If true, it shows detailed forecast numDetails times.</td>
		<td>true</td>
	</tr>
	<tr>
		<td>numDetails</td>
		<td>How many detailed forecasts to show. Default is next two periods.</td>
		<td>2</td>
	</tr>
	<tr>
		<td>title</td>
		<td>Title for the module, if shown.</td>
		<td>Værmelding for Steinkjer</td>
	</tr>
	<tr>
		<td>header</td>
		<td>Show header or not. Contents of header is title.</td>
		<td>false</td>
	</tr>
</table>

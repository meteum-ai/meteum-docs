## Queries {#group-Operations-Queries}

###  serverTime  {#query-serverTime}

##### Description

<p>Current time on the server.</p>

##### Response

<p> Returns a
                  <a href="#definition-Time">Time!</a>
                </p>

#### Example

##### Query

<pre><code class="hljs language-gql"><span class="hljs-symbol"><span class="hljs-keyword">query</span> serverTime <span class="hljs-tag">{
  <span class="hljs-symbol">serverTime</span>
}</span></span>
</code></pre> 

##### Response

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;data&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span>
    <span class="hljs-attr">&#34;serverTime&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span>
  <span class="hljs-punctuation">}</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

###  serverTimestamp  {#query-serverTimestamp}

##### Description

<p>Current time on the server.</p>

##### Response

<p> Returns a
                  <a href="#definition-Timestamp">Timestamp!</a>
                </p>

#### Example

##### Query

<pre><code class="hljs language-gql"><span class="hljs-symbol"><span class="hljs-keyword">query</span> serverTimestamp <span class="hljs-tag">{
  <span class="hljs-symbol">serverTimestamp</span>
}</span></span>
</code></pre> 

##### Response

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;data&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;serverTimestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">}</span><span class="hljs-punctuation">}</span>
</code></pre> 

###  stations  {#query-stations}

##### Description

<p>List of weather stations values.</p>

##### Response

<p> Returns
                  <a href="#definition-Station">[Station!]!</a>
                </p>

##### Arguments

<table>
                  <thead>
                    <tr>
                      <th>Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <span class="property-name"><code>minLat</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>maxLat</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>minLon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>maxLon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>language</code></span> -
                        <span class="property-type">
                          <a href="#definition-Language">Language</a>
                        </span>
                      </td>
                      <td>  </td>
                    </tr>
                  </tbody>
                </table>

#### Example

##### Query

<pre><code class="hljs language-gql"><span class="hljs-symbol"><span class="hljs-keyword">query</span> stations<span class="hljs-tag">(
  <span class="hljs-code">$minLat</span>:<span class="hljs-type"> Float!</span>,
  <span class="hljs-code">$maxLat</span>:<span class="hljs-type"> Float!</span>,
  <span class="hljs-code">$minLon</span>:<span class="hljs-type"> Float!</span>,
  <span class="hljs-code">$maxLon</span>:<span class="hljs-type"> Float!</span>,
  <span class="hljs-code">$language</span>:<span class="hljs-type"> Language
</span>)</span> <span class="hljs-tag">{
  <span class="hljs-symbol">stations<span class="hljs-tag">(
    minLat: <span class="hljs-code">$minLat</span>,
    maxLat: <span class="hljs-code">$maxLat</span>,
    minLon: <span class="hljs-code">$minLon</span>,
    maxLon: <span class="hljs-code">$maxLon</span>,
    language: <span class="hljs-code">$language</span>
  )</span> <span class="hljs-tag">{
    <span class="hljs-symbol">id</span>
    <span class="hljs-symbol">code</span>
    <span class="hljs-symbol">name</span>
    <span class="hljs-symbol">lat</span>
    <span class="hljs-symbol">lon</span>
    <span class="hljs-symbol">time</span>
    <span class="hljs-symbol">timestamp</span>
    <span class="hljs-symbol">cloudiness</span>
    <span class="hljs-symbol">condition</span>
    <span class="hljs-symbol">distance</span>
    <span class="hljs-symbol">feelsLike</span>
    <span class="hljs-symbol">humidity</span>
    <span class="hljs-symbol">icon</span>
    <span class="hljs-symbol">isThunder</span>
    <span class="hljs-symbol">phenomCondition</span>
    <span class="hljs-symbol">phenomIcon</span>
    <span class="hljs-symbol">prec</span>
    <span class="hljs-symbol">precProbability</span>
    <span class="hljs-symbol">precStrength</span>
    <span class="hljs-symbol">precType</span>
    <span class="hljs-symbol">pressure</span>
    <span class="hljs-symbol">temperature</span>
    <span class="hljs-symbol">waterTemperature</span>
    <span class="hljs-symbol">windAngle</span>
    <span class="hljs-symbol">windDirection</span>
    <span class="hljs-symbol">windSpeed</span>
  }</span></span>
}</span></span>
</code></pre> 

##### Variables

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;minLat&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">47.27319717</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxLat&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">47.27319717</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;minLon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">-119.7085724</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxLon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">-119.7085724</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;language&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;EN&#34;</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

##### Response

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;data&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span>
    <span class="hljs-attr">&#34;stations&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span>
      <span class="hljs-punctuation">{</span>
        <span class="hljs-attr">&#34;id&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">123</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;code&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;xyz789&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;name&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;abc123&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;lat&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">47.27319717</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;lon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">-119.7085724</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;time&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;timestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;cloudiness&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;condition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;distance&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">987.65</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;feelsLike&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;icon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;isThunder&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-literal"><span class="hljs-keyword">false</span></span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;phenomCondition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;BLOWING_SNOW&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;phenomIcon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;precProbability&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;precStrength&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;ZERO&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;precType&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;NO_TYPE&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;temperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
      <span class="hljs-punctuation">}</span>
    <span class="hljs-punctuation">]</span>
  <span class="hljs-punctuation">}</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

###  stationsByTimeRange  {#query-stationsByTimeRange}

##### Description

<p>List of weather stations values by time range.</p>

##### Response

<p> Returns
                  <a href="#definition-Station">[Station!]!</a>
                </p>

##### Arguments

<table>
                  <thead>
                    <tr>
                      <th>Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <span class="property-name"><code>request</code></span> -
                        <span class="property-type">
                          <a href="#definition-PointInput">PointInput!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>timeRange</code></span> -
                        <span class="property-type">
                          <a href="#definition-TimeRange">TimeRange!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

#### Example

##### Query

<pre><code class="hljs language-gql"><span class="hljs-symbol"><span class="hljs-keyword">query</span> stationsByTimeRange<span class="hljs-tag">(
  <span class="hljs-code">$request</span>:<span class="hljs-type"> PointInput!</span>,
  <span class="hljs-code">$timeRange</span>:<span class="hljs-type"> TimeRange!</span>
)</span> <span class="hljs-tag">{
  <span class="hljs-symbol">stationsByTimeRange<span class="hljs-tag">(
    request: <span class="hljs-code">$request</span>,
    timeRange: <span class="hljs-code">$timeRange</span>
  )</span> <span class="hljs-tag">{
    <span class="hljs-symbol">id</span>
    <span class="hljs-symbol">code</span>
    <span class="hljs-symbol">name</span>
    <span class="hljs-symbol">lat</span>
    <span class="hljs-symbol">lon</span>
    <span class="hljs-symbol">time</span>
    <span class="hljs-symbol">timestamp</span>
    <span class="hljs-symbol">cloudiness</span>
    <span class="hljs-symbol">condition</span>
    <span class="hljs-symbol">distance</span>
    <span class="hljs-symbol">feelsLike</span>
    <span class="hljs-symbol">humidity</span>
    <span class="hljs-symbol">icon</span>
    <span class="hljs-symbol">isThunder</span>
    <span class="hljs-symbol">phenomCondition</span>
    <span class="hljs-symbol">phenomIcon</span>
    <span class="hljs-symbol">prec</span>
    <span class="hljs-symbol">precProbability</span>
    <span class="hljs-symbol">precStrength</span>
    <span class="hljs-symbol">precType</span>
    <span class="hljs-symbol">pressure</span>
    <span class="hljs-symbol">temperature</span>
    <span class="hljs-symbol">waterTemperature</span>
    <span class="hljs-symbol">windAngle</span>
    <span class="hljs-symbol">windDirection</span>
    <span class="hljs-symbol">windSpeed</span>
  }</span></span>
}</span></span>
</code></pre> 

##### Variables

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;request&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">PointInput</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;timeRange&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">TimeRange</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

##### Response

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;data&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span>
    <span class="hljs-attr">&#34;stationsByTimeRange&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span>
      <span class="hljs-punctuation">{</span>
        <span class="hljs-attr">&#34;id&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">987</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;code&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;xyz789&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;name&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;xyz789&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;lat&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">47.27319717</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;lon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">-119.7085724</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;time&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;timestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;cloudiness&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;condition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;distance&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">123.45</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;feelsLike&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;icon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;isThunder&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-literal"><span class="hljs-keyword">true</span></span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;phenomCondition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;BLOWING_SNOW&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;phenomIcon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;precProbability&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;precStrength&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;ZERO&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;precType&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;NO_TYPE&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;temperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
        <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
      <span class="hljs-punctuation">}</span>
    <span class="hljs-punctuation">]</span>
  <span class="hljs-punctuation">}</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

###  weatherByPoint  {#query-weatherByPoint}

##### Description

<p>Weather for a geographical point with <code>lat</code> and <code>lon</code> coordinates.</p>

##### Response

<p> Returns a
                  <a href="#definition-Weather">Weather!</a>
                </p>

##### Arguments

<table>
                  <thead>
                    <tr>
                      <th>Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <span class="property-name"><code>request</code></span> -
                        <span class="property-type">
                          <a href="#definition-PointInput">PointInput!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>language</code></span> -
                        <span class="property-type">
                          <a href="#definition-Language">Language</a>
                        </span>
                      </td>
                      <td>  </td>
                    </tr>
                  </tbody>
                </table>

#### Example

##### Query

<pre><code class="hljs language-gql"><span class="hljs-symbol"><span class="hljs-keyword">query</span> weatherByPoint<span class="hljs-tag">(
  <span class="hljs-code">$request</span>:<span class="hljs-type"> PointInput!</span>,
  <span class="hljs-code">$language</span>:<span class="hljs-type"> Language
</span>)</span> <span class="hljs-tag">{
  <span class="hljs-symbol">weatherByPoint<span class="hljs-tag">(
    request: <span class="hljs-code">$request</span>,
    language: <span class="hljs-code">$language</span>
  )</span> <span class="hljs-tag">{
    <span class="hljs-symbol">climate <span class="hljs-tag">{
      <span class="hljs-symbol">days <span class="hljs-tag">{
        <span class="hljs-type">...ClimateDayFragment</span>
      }</span></span>
      <span class="hljs-symbol">weeks <span class="hljs-tag">{
        <span class="hljs-type">...ClimateWeekFragment</span>
      }</span></span>
      <span class="hljs-symbol">months <span class="hljs-tag">{
        <span class="hljs-type">...ClimateMonthFragment</span>
      }</span></span>
      <span class="hljs-symbol">zone <span class="hljs-tag">{
        <span class="hljs-type">...ClimateZoneFragment</span>
      }</span></span>
    }</span></span>
    <span class="hljs-symbol">forecast <span class="hljs-tag">{
      <span class="hljs-symbol">days <span class="hljs-tag">{
        <span class="hljs-type">...ForecastDayFragment</span>
      }</span></span>
      <span class="hljs-symbol">hours <span class="hljs-tag">{
        <span class="hljs-type">...ForecastHoursConnectionFragment</span>
      }</span></span>
    }</span></span>
    <span class="hljs-symbol">location <span class="hljs-tag">{
      <span class="hljs-symbol">altitude</span>
      <span class="hljs-symbol">lat</span>
      <span class="hljs-symbol">lon</span>
      <span class="hljs-symbol">pressureNorm</span>
      <span class="hljs-symbol">timezone <span class="hljs-tag">{
        <span class="hljs-type">...TimezoneFragment</span>
      }</span></span>
    }</span></span>
    <span class="hljs-symbol">now <span class="hljs-tag">{
      <span class="hljs-symbol">cloudiness</span>
      <span class="hljs-symbol">condition</span>
      <span class="hljs-symbol">daytime</span>
      <span class="hljs-symbol">feelsLike</span>
      <span class="hljs-symbol">humidity</span>
      <span class="hljs-symbol">icon</span>
      <span class="hljs-symbol">isThunder</span>
      <span class="hljs-symbol">phenomCondition</span>
      <span class="hljs-symbol">phenomIcon</span>
      <span class="hljs-symbol">pollution <span class="hljs-tag">{
        <span class="hljs-type">...PollutionFragment</span>
      }</span></span>
      <span class="hljs-symbol">precProbability</span>
      <span class="hljs-symbol">precStrength</span>
      <span class="hljs-symbol">precType</span>
      <span class="hljs-symbol">pressure</span>
      <span class="hljs-symbol">season</span>
      <span class="hljs-symbol">soilMoisture</span>
      <span class="hljs-symbol">soilTemperature</span>
      <span class="hljs-symbol">temperature</span>
      <span class="hljs-symbol">uvIndex</span>
      <span class="hljs-symbol">waterTemperature</span>
      <span class="hljs-symbol">waveAngle</span>
      <span class="hljs-symbol">waveDirection</span>
      <span class="hljs-symbol">waveHeight</span>
      <span class="hljs-symbol">wavePeriod</span>
      <span class="hljs-symbol">windAngle</span>
      <span class="hljs-symbol">windDirection</span>
      <span class="hljs-symbol">windGust</span>
      <span class="hljs-symbol">windSpeed</span>
    }</span></span>
    <span class="hljs-symbol">url</span>
  }</span></span>
}</span></span>
</code></pre> 

##### Variables

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;request&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">PointInput</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;language&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;EN&#34;</span><span class="hljs-punctuation">}</span>
</code></pre> 

##### Response

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;data&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span>
    <span class="hljs-attr">&#34;weatherByPoint&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span>
      <span class="hljs-attr">&#34;climate&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Climate</span><span class="hljs-punctuation">,</span>
      <span class="hljs-attr">&#34;forecast&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Forecast</span><span class="hljs-punctuation">,</span>
      <span class="hljs-attr">&#34;location&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Location</span><span class="hljs-punctuation">,</span>
      <span class="hljs-attr">&#34;now&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Now</span><span class="hljs-punctuation">,</span>
      <span class="hljs-attr">&#34;url&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;https://meteum.ai/london&#34;</span>
    <span class="hljs-punctuation">}</span>
  <span class="hljs-punctuation">}</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

## Types {#group-Types}

### Boolean {#definition-Boolean}

##### Description

<p>The <code>Boolean</code> scalar type represents <code>true</code> or <code>false</code>.</p>

##### Example

<pre><code class="hljs language-json"><span class="hljs-literal"><span class="hljs-keyword">true</span></span>
</code></pre> 

### Climate {#definition-Climate}

##### Description

<p>Average weather statistics for 10 years.</p>

##### Fields Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>days</code></span> -
                        <span class="property-type">
                          <a href="#definition-ClimateDay">[ClimateDay!]!</a>
                        </span>
                      </td>
                      <td> Statistics grouped by day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>offset</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to skip
                                <em>N</em> entries.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>limit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to limit the number of entries returned. In a leap year, 366 days will be returned.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>loop</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Boolean">Boolean</a>
                                </span>
                              </h6>
                              <p>Allows you to loop records. After December 31, it will be followed by January 1.</p>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>weeks</code></span> -
                        <span class="property-type">
                          <a href="#definition-ClimateWeek">[ClimateWeek!]!</a>
                        </span>
                      </td>
                      <td> Statistics grouped by week. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>offset</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to skip
                                <em>N</em> entries.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>limit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to limit the number of entries returned. It always returns no more than 48 possible weeks in a year.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>loop</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Boolean">Boolean</a>
                                </span>
                              </h6>
                              <p>Allows you to loop records. After last week of the year, it will be followed by first week.</p>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>months</code></span> -
                        <span class="property-type">
                          <a href="#definition-ClimateMonth">[ClimateMonth!]!</a>
                        </span>
                      </td>
                      <td> Statistics grouped by month. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>offset</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to skip
                                <em>N</em> entries.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>limit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to limit the number of entries returned. It always returns no more than 12 possible months in a year.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>loop</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Boolean">Boolean</a>
                                </span>
                              </h6>
                              <p>Allows you to loop records. After December, it will be followed by January.</p>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>zone</code></span> -
                        <span class="property-type">
                          <a href="#definition-ClimateZone">ClimateZone!</a>
                        </span>
                      </td>
                      <td> Climate zone description. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;days&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span><span class="hljs-string">ClimateDay</span><span class="hljs-punctuation">]</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;weeks&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span><span class="hljs-string">ClimateWeek</span><span class="hljs-punctuation">]</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;months&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span><span class="hljs-string">ClimateMonth</span><span class="hljs-punctuation">]</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;zone&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">ClimateZone</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ClimateDay {#definition-ClimateDay}

##### Description

<p>Statistics for one day.</p>

##### Fields Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>cloudiness</code></span> -
                        <span class="property-type">
                          <a href="#definition-Cloudiness">Cloudiness!</a>
                        </span>
                      </td>
                      <td> Average cloudiness for this day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>condition</code></span> -
                        <span class="property-type">
                          <a href="#definition-Condition">Condition!</a>
                        </span>
                      </td>
                      <td> The general weather condition that fits to <code>cloudiness</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>feelsLike</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The same temperature values may be perceived differently depending on humidity, wind strength, and ultraviolet radiation. <code>feelsLike</code> shows how comfortable the weather conditions are, taking into account all these factors. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>humidity</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The percentage of the mass fraction of water vapor in the air to the maximum possible at the current temperature. Contains the average value for this day. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>icon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url!</a>
                        </span>
                      </td>
                      <td> Icon describing the general weather condition for this day. Fits to the <code>cloudiness</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>format</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconFormat">IconFormat!</a>
                                </span>
                              </h6>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>theme</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconTheme">IconTheme</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>maxDayTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The highest temperature for this day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>maxWindSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The highest wind speed for this day. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>minNightTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The lowest temperature for this day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>minWindSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The lowest wind speed for this day. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>prec</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Amount of precipitation in this day. Measured in millimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precProbability</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The probability of precipitation for this day. Possible values are in <code>[0, 1]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precStrength</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecStrength">PrecStrength!</a>
                        </span>
                      </td>
                      <td> The highest strength of precipitation for this day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precType</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecType">PrecType!</a>
                        </span>
                      </td>
                      <td> Precipitation corresponding to the precipitation strength. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>pressure</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Atmospheric pressure for this day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-PressureUnit">PressureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>waterTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The water surface temperature for this day. Exists only for cities that are located near large bodies of water. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The angle of the wind direction in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WindDirection">WindDirection!</a>
                        </span>
                      </td>
                      <td> Average wind direction for this day. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;cloudiness&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;condition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;feelsLike&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;icon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxDayTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxWindSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;minNightTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;minWindSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precProbability&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precStrength&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;ZERO&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precType&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;NO_TYPE&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ClimateMonth {#definition-ClimateMonth}

##### Description

<p>Statistics for one month.</p>

##### Fields Arguments  Arguments  Arguments  Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>avgDayTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Average daily temperature for this month. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>humidity</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The percentage of the mass fraction of water vapor in the air to the maximum possible at the current temperature. Contains the average value for this month. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>maxDayTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The highest daily temperature for this month. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>minNightTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The lowest night temperature for this month. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>overcastDays</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The number of cloudy days for this month. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>prec</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Amount of precipitation for this month. Measured in millimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precDays</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The number of days with precipitation for this month. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>pressure</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Average atmospheric pressure for this month. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-PressureUnit">PressureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunnyDays</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Number of sunny days for this month. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>waterTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Average water surface temperature for this month. Exists only for cities that are located near large bodies of water. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Average angle of the wind direction in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WindDirection">WindDirection!</a>
                        </span>
                      </td>
                      <td> Average wind direction for this month. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Average wind speed for this month. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;avgDayTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxDayTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;minNightTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;overcastDays&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precDays&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunnyDays&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ClimateWeek {#definition-ClimateWeek}

##### Description

<p>Statistics for one week.</p>

##### Fields Arguments  Arguments  Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>maxDayTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The highest daily temperature for this week. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>maxWindSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The highest wind speed for this week. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>minNightTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The lowest night temperature for this week. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>prec</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The amount of precipitation for this week. Measured in millimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>strongPrecDays</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Days of this week with heavy precipitation. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunnyDays</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Number of sunny days for this week. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>veryStrongPrecDays</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Days of this week with very heavy precipitation. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>verySunnyDays</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Number of very sunny days for this week. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>waterTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Average water surface temperature for this week. Exists only for cities that are located near large bodies of water. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Average angle of the wind direction in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WindDirection">WindDirection!</a>
                        </span>
                      </td>
                      <td> Average wind direction for this week. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Average wind speed for this week. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;maxDayTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxWindSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;minNightTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;strongPrecDays&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunnyDays&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;veryStrongPrecDays&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;verySunnyDays&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ClimateZone {#definition-ClimateZone}

##### Description

<p>Climate zone description.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>code</code></span> -
                        <span class="property-type">
                          <a href="#definition-ClimateZoneCode">ClimateZoneCode!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>description</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;code&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;None&#34;</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;description&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;abc123&#34;</span><span class="hljs-punctuation">}</span>
</code></pre> 

### ClimateZoneCode {#definition-ClimateZoneCode}

##### Description

<p>Represents codes of climate zones. See more here
                  <a href="https://en.wikipedia.org/wiki/K%C3%B6ppen_climate_classification">https://en.wikipedia.org/wiki/Köppen_climate_classification</a>
                </p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>None</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Af</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Am</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Aw</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>BWh</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>BWk</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>BSh</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>BSk</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Csa</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Csb</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Csc</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Cwa</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Cwb</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Cwc</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Cfa</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Cfb</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Cfc</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dsa</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dsb</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dsc</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dsd</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dwa</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dwb</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dwc</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dwd</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dfa</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dfb</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dfc</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>Dfd</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>ET</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>EF</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;None&#34;</span>
</code></pre> 

### Cloudiness {#definition-Cloudiness}

##### Description

<p>Represents the state of cloudiness. In ascending order: <code>CLEAR</code> – minimum, <code>OVERCAST</code> – maximum.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>CLEAR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PARTLY</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SIGNIFICANT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>CLOUDY</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>OVERCAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;CLEAR&#34;</span>
</code></pre> 

### Condition {#definition-Condition}

##### Description

<p>Represents the general weather conditions.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>CLEAR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PARTLY_CLOUDY</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>CLOUDY</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>OVERCAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>LIGHT_RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>HEAVY_RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SHOWERS</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SLEET</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>LIGHT_SNOW</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SNOW</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SNOWFALL</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>HAIL</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>THUNDERSTORM</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>THUNDERSTORM_WITH_RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>THUNDERSTORM_WITH_HAIL</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;CLEAR&#34;</span>
</code></pre> 

### Datum {#definition-Datum}

##### Description

<p>Supported datum options.
                  <a href="https://tidesandcurrents.noaa.gov/datum_options.html">https://tidesandcurrents.noaa.gov/datum_options.html</a>
                </p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>MSL</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>LAT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>MLLW</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;MSL&#34;</span>
</code></pre> 

### Daypart {#definition-Daypart}

##### Description

<p>Aggregations for one time of day. Be careful, some of the fields may be skipped.</p>

##### Fields Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>avgTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Average temperature value for this time of day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>cloudiness</code></span> -
                        <span class="property-type">
                          <a href="#definition-Cloudiness">Cloudiness!</a>
                        </span>
                      </td>
                      <td> Average cloudiness for this time of day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>condition</code></span> -
                        <span class="property-type">
                          <a href="#definition-Condition">Condition!</a>
                        </span>
                      </td>
                      <td> The general weather condition that fits to <code>cloudiness</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>daytime</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daytime">Daytime!</a>
                        </span>
                      </td>
                      <td> Indicates the presence of the sun most of the time during the aggregation period. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>feelsLike</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The same temperature values may be perceived differently depending on humidity, wind strength, and ultraviolet radiation. <code>feelsLike</code> shows how comfortable the weather conditions are, taking into account all these factors. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>freshSnow</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> Amount of fresh snow in this time of day. Measured in millimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>humidity</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The percentage of the mass fraction of water vapor in the air to the maximum possible at the current temperature. Contains the average value for time of day. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>icon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url!</a>
                        </span>
                      </td>
                      <td> Icon describing the general weather condition. Fits to the <code>cloudiness</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>format</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconFormat">IconFormat!</a>
                                </span>
                              </h6>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>theme</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconTheme">IconTheme</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>maxSoilTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Highest soil temperature at a depth of 10 meters. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>minSoilTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Lowest soil temperature at a depth of 10 meters. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>maxTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Highest temperature value for this time of day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>minTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Lowest temperature value for this time of day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>prec</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Amount of precipitation in this time of day. Measured in millimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precProbability</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> The probability of precipitation for this time of day. Possible values are in <code>[0, 1]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precStrength</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecStrength">PrecStrength!</a>
                        </span>
                      </td>
                      <td> Highest strength of precipitation for this time of day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precType</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecType">PrecType!</a>
                        </span>
                      </td>
                      <td> Precipitation corresponding to the precipitation strength. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>pressure</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Atmospheric pressure for this time of day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-PressureUnit">PressureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>soilMoisture</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> Median percentage of all soil moisture to dry soil. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>soilTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Median soil temperature at a depth of 7 cm. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>temperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Contains the temperature value that is more suitable for this time of day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>uvIndex</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The level of solar radiation on the Earth&#39;s surface. Possible values are in <code>[0, 13]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>visibility</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Visibility in meters for this time of day. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>waterTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Highest water surface temperature for this time of day. Exists only for cities that are located near large bodies of water. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The angle of the wind direction in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WindDirection">WindDirection!</a>
                        </span>
                      </td>
                      <td> Wind direction for this time of day. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windGust</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Highest speed of wind gusts for this time of day. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Highest wind speed for this time of day. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;avgTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">123</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;cloudiness&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;condition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;daytime&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;DAY&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;feelsLike&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;freshSnow&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;icon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxSoilTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;minSoilTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;maxTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;minTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precProbability&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precStrength&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;ZERO&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precType&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;NO_TYPE&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;soilMoisture&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;soilTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;temperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;uvIndex&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">2</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;visibility&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">123</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windGust&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### Dayparts {#definition-Dayparts}

##### Description

<p>Summary for four parts of the day. Use this aggregations when you divide the day into morning, afternoon, evening, and night.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>night</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daypart">Daypart!</a>
                        </span>
                      </td>
                      <td> Night aggregations. Be careful, it is the night before the morning of the current day. If you need a night after the evening of the current day, take the night from the next day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>morning</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daypart">Daypart!</a>
                        </span>
                      </td>
                      <td> Morning aggregations. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>day</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daypart">Daypart!</a>
                        </span>
                      </td>
                      <td> Afternoon aggregations. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>evening</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daypart">Daypart!</a>
                        </span>
                      </td>
                      <td> Evening aggregations </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;night&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Daypart</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;morning&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Daypart</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;day&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Daypart</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;evening&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Daypart</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### Daytime {#definition-Daytime}

##### Description

<p>Represents the time of day.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>DAY</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>NIGHT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;DAY&#34;</span>
</code></pre> 

### Float {#definition-Float}

##### Description

<p>The <code>Float</code> scalar type represents signed double-precision fractional values as specified by
                  <a href="https://en.wikipedia.org/wiki/IEEE_floating_point">IEEE 754</a>.</p>

##### Example

<pre><code class="hljs language-json"><span class="hljs-number">987.65</span>
</code></pre> 

### Forecast {#definition-Forecast}

##### Description

<p>The main weather forecast.</p>

##### Fields Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>days</code></span> -
                        <span class="property-type">
                          <a href="#definition-ForecastDay">[ForecastDay!]!</a>
                        </span>
                      </td>
                      <td> Forecasts grouped by day. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>offset</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to skip
                                <em>N</em> entries.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>limit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int</a>
                                </span>
                              </h6>
                              <p>Allows you to limit the number of entries returned.</p>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>hours</code></span> -
                        <span class="property-type">
                          <a href="#definition-ForecastHoursConnection">ForecastHoursConnection!</a>
                        </span>
                      </td>
                      <td> Forecasts in plain list. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>first</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Int">Int!</a>
                                </span>
                              </h6>
                              <p>Returns the first
                                <em>N</em> entries from the list.</p>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>after</code></span> -
                                <span class="property-type">
                                  <a href="#definition-String">String</a>
                                </span>
                              </h6>
                              <p>Returns the entries in the list that come after the specified cursor. Cursor can be retrieved from <code>edges.cursor</code>.</p>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;days&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span><span class="hljs-string">ForecastDay</span><span class="hljs-punctuation">]</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;hours&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">ForecastHoursConnection</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ForecastDay {#definition-ForecastDay}

##### Description

<p>Forecast for one day.</p>

##### Fields Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>hours</code></span> -
                        <span class="property-type">
                          <a href="#definition-ForecastHour">[ForecastHour!]!</a>
                        </span>
                      </td>
                      <td> Forecast hours list for this day. Be careful, the size of this list may be less than 24 due to the decreasing frequency of forecasts for distant days. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>kpIndex</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Magnetic field Kp-index. Possible values are in <code>[0, 10]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>moon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Moon phase. Possible values are in <code>[0, 15]</code>. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>oceanTideExtremums</code></span> -
                        <span class="property-type">
                          <a href="#definition-OceanTideExtremumItem">[OceanTideExtremumItem!]</a>
                        </span>
                      </td>
                      <td> The ocean water level maximums and minimums in day </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>datum</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Datum">Datum</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>parts</code></span> -
                        <span class="property-type">
                          <a href="#definition-Dayparts">Dayparts!</a>
                        </span>
                      </td>
                      <td> Dayparts aggregations for this day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>polar</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daytime">Daytime</a>
                        </span>
                      </td>
                      <td> Indicates the polar day or polar night. Skipped when the day is normal. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>summary</code></span> -
                        <span class="property-type">
                          <a href="#definition-Summary">Summary!</a>
                        </span>
                      </td>
                      <td> Summary aggregations for this day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="" class="definition-deprecated">
                        <span class="property-name"><code>sunrise</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> Sunrise time in format <code>hh:mm</code>.
                        <span class="deprecation-reason">use <code>sunriseTime</code> field</span>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunriseTime</code></span> -
                        <span class="property-type">
                          <a href="#definition-Time">Time!</a>
                        </span>
                      </td>
                      <td> Sunrise time. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunriseTimestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> Sunrise time. </td>
                    </tr>
                    <tr>
                      <td data-property-name="" class="definition-deprecated">
                        <span class="property-name"><code>sunriseBegin</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> Start time of the sunrise in format <code>hh:mm</code>.
                        <span class="deprecation-reason">use <code>sunriseBeginTime</code> field</span>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunriseBeginTime</code></span> -
                        <span class="property-type">
                          <a href="#definition-Time">Time!</a>
                        </span>
                      </td>
                      <td> Start time of the sunrise. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunriseBeginTimestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> Start time of the sunrise. </td>
                    </tr>
                    <tr>
                      <td data-property-name="" class="definition-deprecated">
                        <span class="property-name"><code>sunset</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> Sunset time in format <code>hh:mm</code>.
                        <span class="deprecation-reason">use <code>sunsetTime</code> field</span>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunsetTime</code></span> -
                        <span class="property-type">
                          <a href="#definition-Time">Time!</a>
                        </span>
                      </td>
                      <td> Sunset time. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunsetTimestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> Sunset time. </td>
                    </tr>
                    <tr>
                      <td data-property-name="" class="definition-deprecated">
                        <span class="property-name"><code>sunsetEnd</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> End time of the sunset in format <code>hh:mm</code>.
                        <span class="deprecation-reason">use <code>sunsetEndTime</code> field</span>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunsetEndTime</code></span> -
                        <span class="property-type">
                          <a href="#definition-Time">Time!</a>
                        </span>
                      </td>
                      <td> End time of the sunset. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>sunsetEndTimestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> End time of the sunset. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>time</code></span> -
                        <span class="property-type">
                          <a href="#definition-Time">Time!</a>
                        </span>
                      </td>
                      <td> Start time of the day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>timestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> Start time of the day. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;hours&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span><span class="hljs-string">ForecastHour</span><span class="hljs-punctuation">]</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;kpIndex&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">2</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;moon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">2</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;oceanTideExtremums&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span><span class="hljs-string">OceanTideExtremumItem</span><span class="hljs-punctuation">]</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;parts&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Dayparts</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;polar&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;DAY&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;summary&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Summary</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunrise&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;10:30&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunriseTime&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunriseTimestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunriseBegin&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;10:30&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunriseBeginTime&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunriseBeginTimestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunset&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;10:30&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunsetTime&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunsetTimestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunsetEnd&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;10:30&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunsetEndTime&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;sunsetEndTimestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;time&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;timestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ForecastHour {#definition-ForecastHour}

##### Description

<p>One hour of the forecast. Can contains data from Meteum, Nowcast, and others.</p>

##### Fields Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>cloudiness</code></span> -
                        <span class="property-type">
                          <a href="#definition-Cloudiness">Cloudiness!</a>
                        </span>
                      </td>
                      <td> Сloudiness for this hour. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>condition</code></span> -
                        <span class="property-type">
                          <a href="#definition-Condition">Condition!</a>
                        </span>
                      </td>
                      <td> The general weather condition that fits to <code>cloudiness</code>, <code>isThunder</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>feelsLike</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The same temperature values may be perceived differently depending on humidity, wind strength, and ultraviolet radiation. <code>feelsLike</code> shows how comfortable the weather conditions are, taking into account all these factors. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>humidity</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The percentage of the mass fraction of water vapor in the air to the maximum possible at the current temperature. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>icon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url!</a>
                        </span>
                      </td>
                      <td> Icon describing the general weather condition. Fits to the <code>cloudiness</code>, <code>isThunder</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>format</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconFormat">IconFormat!</a>
                                </span>
                              </h6>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>theme</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconTheme">IconTheme</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>isThunder</code></span> -
                        <span class="property-type">
                          <a href="#definition-Boolean">Boolean!</a>
                        </span>
                      </td>
                      <td> Flag showing the presence of a thunder for the current hour. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>oceanTide</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> The height of the ocean water level relative to the specified datum in centimeters. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>datum</code></span> -
                                <span class="property-type">
                                  <a href="#definition-Datum">Datum</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>pollution</code></span> -
                        <span class="property-type">
                          <a href="#definition-Pollution">Pollution</a>
                        </span>
                      </td>
                      <td> Atmospheric composition forecast for this hour. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>prec</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Amount of precipitation in this hour. Measured in millimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precProbability</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> The probability of precipitation for this hour. Possible values are in <code>[0, 1]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precStrength</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecStrength">PrecStrength!</a>
                        </span>
                      </td>
                      <td> The strength of precipitation for this hour. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precType</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecType">PrecType!</a>
                        </span>
                      </td>
                      <td> The type of precipitation for this hour. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>pressure</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Atmospheric pressure for this hour. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-PressureUnit">PressureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>surfaceTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The temperature of the surface of the Earth for this hour. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>soilMoisture</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> The percentage of all soil moisture to dry soil. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>soilTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Soil temperature at a depth of 7 cm. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>solarIrradiation</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> Average direct solar irradiation on the horizontal plane Measured in W/m^2.
                        <a href="https://en.wikipedia.org/wiki/Solar_irradiance">https://en.wikipedia.org/wiki/Solar_irradiance</a>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>temperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The temperature value in the shade at a height of 2 meters from the ground surface. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>time</code></span> -
                        <span class="property-type">
                          <a href="#definition-Time">Time!</a>
                        </span>
                      </td>
                      <td> Forecast horizon time. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>timestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> Forecast horizon time. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>uvIndex</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The level of solar radiation on the Earth&#39;s surface. Possible values are in <code>[0, 13]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>visibility</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Visibility in meters. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>waterTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The water surface temperature. Exists only for cities that are located near large bodies of water. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>waveAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The angle in which the primary wave is moving. Measured in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>waveDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WaveDirection">WaveDirection</a>
                        </span>
                      </td>
                      <td> The direction in which the primary wave is moving. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>waveHeight</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> Significant height of combined wind waves and swell surface. Measured in meters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>wavePeriod</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Primary wave mean period surface. Measured in seconds. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The angle of the wind direction in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WindDirection">WindDirection!</a>
                        </span>
                      </td>
                      <td> Wind direction for this hour. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windGust</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The speed of wind gusts. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Wind speed at a height of 10 meters from the ground surface. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;cloudiness&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;condition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;feelsLike&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;icon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;isThunder&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-literal"><span class="hljs-keyword">true</span></span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;oceanTide&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pollution&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Pollution</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precProbability&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precStrength&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;ZERO&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precType&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;NO_TYPE&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;surfaceTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;soilMoisture&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;soilTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;solarIrradiation&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">987.65</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;temperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;time&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;timestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;uvIndex&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">2</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;visibility&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">123</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waveAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waveDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waveHeight&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;wavePeriod&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windGust&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ForecastHoursConnection {#definition-ForecastHoursConnection}

##### Description

<p>The connection type for <code>ForecastHour</code>.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>edges</code></span> -
                        <span class="property-type">
                          <a href="#definition-ForecastHoursEdge">[ForecastHoursEdge!]!</a>
                        </span>
                      </td>
                      <td> A list of edges. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>pageInfo</code></span> -
                        <span class="property-type">
                          <a href="#definition-PageInfo">PageInfo!</a>
                        </span>
                      </td>
                      <td> Information to aid in pagination. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;edges&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">[</span><span class="hljs-string">ForecastHoursEdge</span><span class="hljs-punctuation">]</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pageInfo&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">PageInfo</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### ForecastHoursEdge {#definition-ForecastHoursEdge}

##### Description

<p>An edge in a connection.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>cursor</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> The cursor pointing to the entry. It can be used in future queries for paging. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>node</code></span> -
                        <span class="property-type">
                          <a href="#definition-ForecastHour">ForecastHour!</a>
                        </span>
                      </td>
                      <td> The item at the end of the edge. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;cursor&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;xyz789&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;node&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">ForecastHour</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### IconFormat {#definition-IconFormat}

##### Description

<p>Represents the icon format. If you need a fixed-size png, use <code>PNG_{size}</code>. If you need only code, use <code>CODE</code>.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>CODE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PNG_24</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PNG_32</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PNG_48</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PNG_64</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PNG_96</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PNG_112</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PNG_128</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SVG</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;CODE&#34;</span>
</code></pre> 

### IconTheme {#definition-IconTheme}

##### Description

<p>Represents the theme of the icon. Be careful, some icons may not exist in a particular theme.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>BLACK</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>CIRCLE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>DARK</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>FLAT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>LIGHT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>OUTLINE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;BLACK&#34;</span>
</code></pre> 

### Int {#definition-Int}

##### Description

<p>The <code>Int</code> scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.</p>

##### Example

<pre><code class="hljs language-json"><span class="hljs-number">123</span>
</code></pre> 

### Language {#definition-Language}

##### Description

<p>Represents all available Weather languages. The language will be used in texts.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>BE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>DE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>EN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>ES</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>ES_LA</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>FR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>HU</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>ID</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>IT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>KK</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>MK</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PL</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PT_BR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>RO</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>RU</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>TR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>TT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>UK</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>UZ</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">EN</span>
</code></pre> 

### Location {#definition-Location}

##### Description

<p>All information about requested location or point.</p>

##### Fields Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>altitude</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Altitude of this location from topography data source. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>lat</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Latitude of this location. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>lon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Longitude of this location. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>pressureNorm</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Info about normal pressure values for this location. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-PressureUnit">PressureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>timezone</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timezone">Timezone!</a>
                        </span>
                      </td>
                      <td> Timezone information for this location. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;altitude&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">123</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;lat&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">47.27319717</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;lon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">-119.7085724</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pressureNorm&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;timezone&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Timezone</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### Now {#definition-Now}

##### Description

<p>Weather now. It can be compiled from many sources based on different business logic. If you need the actual weather values, then use the data from the <code>Query.stations</code>.</p>

##### Fields Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>cloudiness</code></span> -
                        <span class="property-type">
                          <a href="#definition-Cloudiness">Cloudiness!</a>
                        </span>
                      </td>
                      <td> Current value of cloudiness. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>condition</code></span> -
                        <span class="property-type">
                          <a href="#definition-Condition">Condition!</a>
                        </span>
                      </td>
                      <td> Current general weather condition that fits to <code>cloudiness</code>, <code>isThunder</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>daytime</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daytime">Daytime!</a>
                        </span>
                      </td>
                      <td> Indicates the presence of the sun right now. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>feelsLike</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The same temperature values may be perceived differently depending on humidity, wind strength, and ultraviolet radiation. <code>feelsLike</code> shows how comfortable the weather conditions are, taking into account all these factors. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>humidity</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The percentage of the mass fraction of water vapor in the air to the maximum possible at the current temperature. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>icon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url!</a>
                        </span>
                      </td>
                      <td> Icon describing the general weather condition. Fits to the <code>cloudiness</code>, <code>isThunder</code>, <code>precStrength</code> and <code>precType</code>. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>format</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconFormat">IconFormat!</a>
                                </span>
                              </h6>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>theme</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconTheme">IconTheme</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>isThunder</code></span> -
                        <span class="property-type">
                          <a href="#definition-Boolean">Boolean!</a>
                        </span>
                      </td>
                      <td> Flag showing the presence of a thunder right now (or for some short time period). </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>phenomCondition</code></span> -
                        <span class="property-type">
                          <a href="#definition-PhenomCondition">PhenomCondition</a>
                        </span>
                      </td>
                      <td> Current phenomenon. Skipped when weather conditions are normal. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>phenomIcon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url</a>
                        </span>
                      </td>
                      <td> Icon of the phenomenon. Skipped when weather conditions are normal. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>format</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconFormat">IconFormat!</a>
                                </span>
                              </h6>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>theme</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconTheme">IconTheme</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>pollution</code></span> -
                        <span class="property-type">
                          <a href="#definition-Pollution">Pollution</a>
                        </span>
                      </td>
                      <td> The current composition of the atmosphere. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precProbability</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Current probability of precipitation. Possible values are in <code>[0, 1]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precStrength</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecStrength">PrecStrength!</a>
                        </span>
                      </td>
                      <td> Current value of precipitation strength. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precType</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecType">PrecType!</a>
                        </span>
                      </td>
                      <td> Current type of precipitation. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>pressure</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Current atmospheric pressure. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-PressureUnit">PressureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>season</code></span> -
                        <span class="property-type">
                          <a href="#definition-Season">Season!</a>
                        </span>
                      </td>
                      <td> Current time of year. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>soilMoisture</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> The percentage of all soil moisture to dry soil. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>soilTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Soil temperature at a depth of 7 cm. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>temperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The temperature value in the shade at a height of 2 meters from the ground surface. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>uvIndex</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The level of solar radiation on the Earth&#39;s surface. Possible values are in <code>[0, 13]</code>. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>waterTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The water surface temperature. Exists only for cities that are located near large bodies of water. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>waveAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The angle in which the primary wave is moving. Measured in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>waveDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WaveDirection">WaveDirection</a>
                        </span>
                      </td>
                      <td> The direction in which the primary wave is moving. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>waveHeight</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> Significant height of combined wind waves and swell surface. Measured in meters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>wavePeriod</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Primary wave mean period surface. Measured in seconds. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> The angle of the wind direction in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WindDirection">WindDirection!</a>
                        </span>
                      </td>
                      <td> Current wind direction. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windGust</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> The speed of wind gusts. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Wind speed at a height of 10 meters from the ground surface. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;cloudiness&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;condition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;daytime&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;DAY&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;feelsLike&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;icon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;isThunder&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-literal"><span class="hljs-keyword">false</span></span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;phenomCondition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;BLOWING_SNOW&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;phenomIcon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pollution&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Pollution</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precProbability&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precStrength&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;ZERO&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precType&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;NO_TYPE&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;season&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;SPRING&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;soilMoisture&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;soilTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;temperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;uvIndex&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">2</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waveAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waveDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waveHeight&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;wavePeriod&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">20</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windGust&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### OceanTideExtremumItem {#definition-OceanTideExtremumItem}

##### Description

<p>Ocean tide timeline point.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>timestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> Tide timestamp. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>value</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Tide value in centimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>type</code></span> -
                        <span class="property-type">
                          <a href="#definition-OceanTideExtremumType">OceanTideExtremumType!</a>
                        </span>
                      </td>
                      <td> Extemum type. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;timestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;value&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">987.65</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;type&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;MAX&#34;</span><span class="hljs-punctuation">}</span>
</code></pre> 

### OceanTideExtremumType {#definition-OceanTideExtremumType}

##### Description

<p>Ocean tide extremum type.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>MAX</code></p>
                      </td>
                      <td> Maximum from 12 a.m to 12 p.m or from 12 p.m. to 12 a.m. </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>MIN</code></p>
                      </td>
                      <td> Minimum from 12 a.m to 12 p.m or from 12 p.m. to 12 a.m. </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>USUAL</code></p>
                      </td>
                      <td> Just local extremum. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;MAX&#34;</span>
</code></pre> 

### PageInfo {#definition-PageInfo}

##### Description

<p>Information about pagination in a connection.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>endCursor</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> Cursor to the last element of page. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>hasNextPage</code></span> -
                        <span class="property-type">
                          <a href="#definition-Boolean">Boolean!</a>
                        </span>
                      </td>
                      <td> Flag indicating the presence of the next page. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;endCursor&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;abc123&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;hasNextPage&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-literal"><span class="hljs-keyword">false</span></span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### PhenomCondition {#definition-PhenomCondition}

##### Description

<p>Represents the phenomenon weather conditions.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>BLOWING_SNOW</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>CONTINUOUS_HEAVY_RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>DRIFTING_SNOW</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>DRIZZLE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>DUST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>DUSTSTORM</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>DUST_SUSPENSION</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>FOG</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>FREEZING_RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>ICE_PELLETS</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>MIST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>MODERATE_RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SMOKE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>THUNDERSTORM_WITH_DUSTSTORM</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>TORNADO</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>VOLCANIC_ASH</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;BLOWING_SNOW&#34;</span>
</code></pre> 

### PointInput {#definition-PointInput}

##### Description

<p>Input for <code>Query.weatherByPoint</code>. Represents a geographical point with <code>lat</code> and <code>lon</code> coordinates.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Input Field</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <span class="property-name"><code>lat</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>lon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;lat&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">47.27319717</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;lon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">-119.7085724</span><span class="hljs-punctuation">}</span>
</code></pre> 

### Pollution {#definition-Pollution}

##### Description

<p>Atmospheric composition forecasts.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>aqi</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Air quality index (AQI). See more here
                        <a href="https://en.wikipedia.org/wiki/Air_quality_index">https://en.wikipedia.org/wiki/Air_quality_index</a>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>co</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Carbon monoxide (CO) is a colorless, highly poisonous, odorless, tasteless, flammable gas that is slightly less dense than air. See more here
                        <a href="https://en.wikipedia.org/wiki/Carbon_monoxide">https://en.wikipedia.org/wiki/Carbon_monoxide</a>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>density</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The density of air or atmospheric density, is the mass per unit volume of Earth&#39;s atmosphere. See more here
                        <a href="https://en.wikipedia.org/wiki/Density_of_air">https://en.wikipedia.org/wiki/Density_of_air</a>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>no2</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> The major sources of anthropogenic emissions of NO2 are combustion processes (heating, power generation, and engines in vehicles and ships). See more here
                        <a href="https://en.wikipedia.org/wiki/Nitrogen_dioxide">https://en.wikipedia.org/wiki/Nitrogen_dioxide</a>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>o3</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Ground-level ozone (O3), also known as surface-level ozone and tropospheric ozone, is a trace gas in the troposphere. See more here
                        <a href="https://en.wikipedia.org/wiki/Ground-level_ozone">https://en.wikipedia.org/wiki/Ground-level_ozone</a>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>pm10</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> PM2.5 is a fine particulate matter, with a diameter of 2.5 micrometers (microns) or less. See more here
                        <a href="https://en.wikipedia.org/wiki/Particulates">https://en.wikipedia.org/wiki/Particulates</a>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>pm2p5</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> PM10 is a suspended large solid particles, with a diameter of 10 micrometers (microns) or less. See more here
                        <a href="https://en.wikipedia.org/wiki/Particulates">https://en.wikipedia.org/wiki/Particulates</a>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>so2</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> SO2 is a colorless gas with a pungent odor, which is formed during the burning of fossil fuels and the melting of mineral ores containing sulfur. See more here
                        <a href="https://en.wikipedia.org/wiki/Sulfur_dioxide">https://en.wikipedia.org/wiki/Sulfur_dioxide</a>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;aqi&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">31</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;co&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">132</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;density&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">1.2</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;no2&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">16</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;o3&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">39</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pm10&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">9</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pm2p5&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">6</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;so2&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### PrecStrength {#definition-PrecStrength}

##### Description

<p>Represents the strength of precipitations. In ascending order: <code>ZERO</code> – minimum, <code>VERY_STRONG</code> – maximum.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>ZERO</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>WEAK</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>AVERAGE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>STRONG</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>VERY_STRONG</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;ZERO&#34;</span>
</code></pre> 

### PrecType {#definition-PrecType}

##### Description

<p>Represents the type of precipitations.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>NO_TYPE</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>RAIN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SLEET</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SNOW</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>HAIL</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;NO_TYPE&#34;</span>
</code></pre> 

### PressureUnit {#definition-PressureUnit}

##### Description

<p>Represents the units of measurement of the pressure value. Can be used to convert to convenient units of measurement. Default unit for this API is <code>MM_HG</code>.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>MBAR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>MM_HG</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>PASCAL</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;MBAR&#34;</span>
</code></pre> 

### Season {#definition-Season}

##### Description

<p>Represents the time of the year.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>SPRING</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SUMMER</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>AUTUMN</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>WINTER</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;SPRING&#34;</span>
</code></pre> 

### Station {#definition-Station}

##### Description

<p>Fact weather values from the station. Be careful, some weather values may be skipped because the station can&#39;t measure them.</p>

##### Fields Arguments  Arguments  Arguments  Arguments  Arguments  Arguments  Arguments 

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>id</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Unique station ID for these values. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>code</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> Unique station code for these values. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>name</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> Unique station name for these values. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>lat</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Latitude of the station location. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>lon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Longitude of the station location. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>time</code></span> -
                        <span class="property-type">
                          <a href="#definition-Time">Time!</a>
                        </span>
                      </td>
                      <td> Time of the last data readout in string. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>timestamp</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> Time of the last data readout. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>cloudiness</code></span> -
                        <span class="property-type">
                          <a href="#definition-Cloudiness">Cloudiness</a>
                        </span>
                      </td>
                      <td> Cloudiness value from this station for this <code>timestamp</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>condition</code></span> -
                        <span class="property-type">
                          <a href="#definition-Condition">Condition</a>
                        </span>
                      </td>
                      <td> Calculated using the same logic as <code>Weather.forecast.hours.condition</code>, but based on the values from this station. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>distance</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float!</a>
                        </span>
                      </td>
                      <td> Distance between the station and the search point. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>feelsLike</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Calculated using the same logic as <code>Weather.forecast.hours.feelsLike</code>, but based on the values from this station. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>humidity</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The percentage of the mass fraction of water vapor in the air to the maximum possible at the current temperature. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>icon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url</a>
                        </span>
                      </td>
                      <td> Calculated using the same logic as <code>Weather.forecast.hours.icon</code>, but based on the values from this station. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>format</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconFormat">IconFormat!</a>
                                </span>
                              </h6>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>theme</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconTheme">IconTheme</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>isThunder</code></span> -
                        <span class="property-type">
                          <a href="#definition-Boolean">Boolean!</a>
                        </span>
                      </td>
                      <td> Flag showing the presence of a thunder for the <code>timestamp</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>phenomCondition</code></span> -
                        <span class="property-type">
                          <a href="#definition-PhenomCondition">PhenomCondition</a>
                        </span>
                      </td>
                      <td> The phenomenon observed from this weather station. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>phenomIcon</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url</a>
                        </span>
                      </td>
                      <td> The phenomenon icon that fits to <code>phenomCondition</code>. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>format</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconFormat">IconFormat!</a>
                                </span>
                              </h6>
                            </div>
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>theme</code></span> -
                                <span class="property-type">
                                  <a href="#definition-IconTheme">IconTheme</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>prec</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> Amount of precipitation. Measured in millimeters. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precProbability</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> The probability of precipitation for this hour. Possible values are in <code>[0, 1]</code>. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precStrength</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecStrength">PrecStrength</a>
                        </span>
                      </td>
                      <td> The strength of precipitation according to the data from the station. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>precType</code></span> -
                        <span class="property-type">
                          <a href="#definition-PrecType">PrecType</a>
                        </span>
                      </td>
                      <td> The type of precipitation according to the data from the station. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>pressure</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> Atmospheric pressure for this hour. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-PressureUnit">PressureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>temperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The temperature value in the shade at a height of 2 meters from the ground surface. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>waterTemperature</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The water surface temperature. Exists only for cities that are located near large bodies of water. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-TemperatureUnit">TemperatureUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windAngle</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int</a>
                        </span>
                      </td>
                      <td> The angle of the wind direction in degrees. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>windDirection</code></span> -
                        <span class="property-type">
                          <a href="#definition-WindDirection">WindDirection</a>
                        </span>
                      </td>
                      <td> Wind direction according to the data from the station. </td>
                    </tr>
                    <tr class="row-has-field-arguments">
                      <td data-property-name="">
                        <span class="property-name"><code>windSpeed</code></span> -
                        <span class="property-type">
                          <a href="#definition-Float">Float</a>
                        </span>
                      </td>
                      <td> Wind speed at a height of 10 meters from the ground surface. Measured in meters per second. </td>
                    </tr>
                    <tr class="row-field-arguments">
                      <td colspan="2">
                        <div class="field-arguments">
                          <div class="field-argument-list">
                            <div class="field-argument">
                              <h6 class="field-argument-name">
                                <span class="property-name"><code>unit</code></span> -
                                <span class="property-type">
                                  <a href="#definition-WindSpeedUnit">WindSpeedUnit</a>
                                </span>
                              </h6>
                            </div>
                          </div>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;id&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">123</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;code&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;xyz789&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;name&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;abc123&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;lat&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">47.27319717</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;lon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">-119.7085724</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;time&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;timestamp&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;cloudiness&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;condition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CLEAR&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;distance&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">987.65</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;feelsLike&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;humidity&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;icon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;isThunder&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-literal"><span class="hljs-keyword">false</span></span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;phenomCondition&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;BLOWING_SNOW&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;phenomIcon&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;skc_d&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;prec&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10.1</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precProbability&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">82</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precStrength&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;ZERO&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;precType&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;NO_TYPE&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;pressure&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">762</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;temperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">15</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;waterTemperature&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">10</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windAngle&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">145</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windDirection&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;CALM&#34;</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;windSpeed&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3.5</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### String {#definition-String}

##### Description

<p>The <code>String</code> scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.</p>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;abc123&#34;</span>
</code></pre> 

### Summary {#definition-Summary}

##### Description

<p>Summary for day and night parts only. Use this aggregations when you divide the day into two parts: day and night.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>night</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daypart">Daypart!</a>
                        </span>
                      </td>
                      <td> Night aggregations. Be careful, it is the night before the morning of the current day. If you need a night after the evening of the current day, take the night from the next day. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>day</code></span> -
                        <span class="property-type">
                          <a href="#definition-Daypart">Daypart!</a>
                        </span>
                      </td>
                      <td> Aggregations for the entire civil day. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;night&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Daypart</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;day&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Daypart</span><span class="hljs-punctuation">}</span>
</code></pre> 

### TemperatureUnit {#definition-TemperatureUnit}

##### Description

<p>Represents the units of measurement of the temperature value. Can be used to convert to convenient units of measurement. Default unit for this API is <code>CELSIUS</code>.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>CELSIUS</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>FAHRENHEIT</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;CELSIUS&#34;</span>
</code></pre> 

### Time {#definition-Time}

##### Description

<p>Time in ISO 8601 format <code>2021-03-30T04:10:02Z</code>.</p>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;2022-10-26T12:37:53.528758212+03:00&#34;</span>
</code></pre> 

### TimeRange {#definition-TimeRange}

##### Description

<p>Time interval [from, to].</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Input Field</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <span class="property-name"><code>from</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <span class="property-name"><code>to</code></span> -
                        <span class="property-type">
                          <a href="#definition-Timestamp">Timestamp!</a>
                        </span>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;from&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;to&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;1666778972&#34;</span><span class="hljs-punctuation">}</span>
</code></pre> 

### Timestamp {#definition-Timestamp}

##### Description

<p>Unix timestamp for UTC timezone.</p>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;1666778972&#34;</span>
</code></pre> 

### Timezone {#definition-Timezone}

##### Description

<p>Information that defines the time zone.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>abbr</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> A well-known abbreviation. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>dst</code></span> -
                        <span class="property-type">
                          <a href="#definition-Boolean">Boolean!</a>
                        </span>
                      </td>
                      <td> Indicates that the timezone is currently daylight saving time (DST). </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>name</code></span> -
                        <span class="property-type">
                          <a href="#definition-String">String!</a>
                        </span>
                      </td>
                      <td> Name from IANA time zone database. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>offset</code></span> -
                        <span class="property-type">
                          <a href="#definition-Int">Int!</a>
                        </span>
                      </td>
                      <td> Offset in seconds (can be negative). </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span><span class="hljs-attr">&#34;abbr&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;BST&#34;</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;dst&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-literal"><span class="hljs-keyword">true</span></span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;name&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;Europe/London&#34;</span><span class="hljs-punctuation">,</span> <span class="hljs-attr">&#34;offset&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-number">3600</span><span class="hljs-punctuation">}</span>
</code></pre> 

### Url {#definition-Url}

##### Description

<p>Always URL with schema, host, path. Query parameters are also possible.</p>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">Url</span>
</code></pre> 

### WaveDirection {#definition-WaveDirection}

##### Description

<p>Represents the direction of the wave in terms of the cardinal directions. To determine the direction more accurately, use <code>waveAngle</code>. The value <code>0</code> of <code>waveAngle</code> corresponds to <code>NORTH</code>, <code>180</code> – <code>SOUTH</code>. The enumeration value <code>CALM</code> is possible when the <code>waveHeight</code> is near <code>0</code>.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>CALM</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>NORTH</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>NORTH_EAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>EAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SOUTH_EAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SOUTH</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SOUTH_WEST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>WEST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>NORTH_WEST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;CALM&#34;</span>
</code></pre> 

### Weather {#definition-Weather}

##### Description

<p>Generic object containing all available types of weather data.</p>

##### Fields

<table>
                  <thead>
                    <tr>
                      <th>Field Name</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>climate</code></span> -
                        <span class="property-type">
                          <a href="#definition-Climate">Climate!</a>
                        </span>
                      </td>
                      <td> Average weather statistics for 10 years. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>forecast</code></span> -
                        <span class="property-type">
                          <a href="#definition-Forecast">Forecast!</a>
                        </span>
                      </td>
                      <td> The main weather forecast. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>location</code></span> -
                        <span class="property-type">
                          <a href="#definition-Location">Location!</a>
                        </span>
                      </td>
                      <td> All information about requested location or point. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>now</code></span> -
                        <span class="property-type">
                          <a href="#definition-Now">Now!</a>
                        </span>
                      </td>
                      <td> Weather now. </td>
                    </tr>
                    <tr>
                      <td data-property-name="">
                        <span class="property-name"><code>url</code></span> -
                        <span class="property-type">
                          <a href="#definition-Url">Url!</a>
                        </span>
                      </td>
                      <td> URL to page of Yandex.Weather for the current request. </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
  <span class="hljs-attr">&#34;climate&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Climate</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;forecast&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Forecast</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;location&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Location</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;now&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">Now</span><span class="hljs-punctuation">,</span>
  <span class="hljs-attr">&#34;url&#34;</span><span class="hljs-punctuation">:</span> <span class="hljs-string">&#34;https://meteum.ai/london&#34;</span>
<span class="hljs-punctuation">}</span>
</code></pre> 

### WindDirection {#definition-WindDirection}

##### Description

<p>Represents the direction of the wind in terms of the cardinal directions. To determine the direction more accurately, use <code>windAngle</code>. The value <code>0</code> of <code>windAngle</code> corresponds to <code>NORTH</code>, <code>180</code> – <code>SOUTH</code>. The enumeration value <code>CALM</code> is possible when the <code>windSpeed</code> is <code>0</code>.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>CALM</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>NORTH</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>NORTH_EAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>EAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SOUTH_EAST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SOUTH</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>SOUTH_WEST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>WEST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>NORTH_WEST</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;CALM&#34;</span>
</code></pre> 

### WindSpeedUnit {#definition-WindSpeedUnit}

##### Description

<p>Represents the units of measurement of the wind speed value. Can be used to convert to convenient units of measurement. Default unit for this API is <code>METERS_PER_SECOND</code>.</p>

##### Values

<table>
                  <thead>
                    <tr>
                      <th>Enum Value</th>
                      <th>Description</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>
                        <p><code>KILOMETERS_PER_HOUR</code></p>
                      </td>
                      <td> </td>
                    </tr>
                    <tr>
                      <td>
                        <p><code>METERS_PER_SECOND</code></p>
                      </td>
                      <td> </td>
                    </tr>
                  </tbody>
                </table>

##### Example

<pre><code class="hljs language-gql"><span class="hljs-symbol">&#34;KILOMETERS_PER_HOUR&#34;</span>
</code></pre> 


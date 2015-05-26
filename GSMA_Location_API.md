**Introduction**

The authorized caller is able to query Location of a mobile device.

**URL format**

https://{serverRoot}/oneapi/location/1/queries/location?address={address}&requestedAccuracy={metres}

**HTTP request**

<table>
<thead>
<tr>
<th id="parameter" style="text-align:left;">Parameter            </th>
<th id="type" style="text-align:left;">Description        </th>
<th id="required" style="text-align:left;">Mandatory or Optional   </th>
</tr>
</thead>

<tbody>


<tr>
<td style="text-align:left;"><p>address</p></td>
<td style="text-align:left;"><p>The MSISDN in tel URI(RFC3966) format of the mobile device to locate. At least one address must be provided. Repeat the address parameter for multiple devices.<br>

"tel:" scheme and "+" identifier must be used for address, and must be URL-escaped.<br>

In the above example, the recipients MSISDN is in tel URI(RFC3966) format. %3A represents ":" and %2B represents "+". Thus tel%3A%2B4605010759 represents tel:+4605010759.

 </p></td>
<td style="text-align:left;"><p>Mandatory</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>requestedAccuracy</p></td>
<td style="text-align:left;"><p> It is the preferred accuracy of the result, in metres. Generally, it takes longer time to retrieve an accurate location than a coarse location
</p></td>
<td style="text-align:left;"><p>Mandatory </p></td>
</tr>

</tbody>
</table>

**HTTP respnose code**
<table>
<thead>
<tr>
<th id="parameter" style="text-align:left;">HTTP status code            </th>
<th id="type" style="text-align:left;">Description        </th>
<th id="required" style="text-align:left;">Note   </th>
</tr>
</thead>

<tbody>


<tr>
<td style="text-align:left;"><p>200 </p></td>
<td style="text-align:left;"><p>Successful </p></td>
<td style="text-align:left;"><p> </p></td>
</tr>
<tr>
<td style="text-align:left;"><p>500 </p></td>
<td style="text-align:left;"><p>Internal server error</p></td>
<td style="text-align:left;"><p> </p></td>
</tr>
<tr>
<td style="text-align:left;"><p>400 </p></td>
<td style="text-align:left;"><p>The syntax of the request is not correct.
 </p></td>
<td style="text-align:left;"><p> </p></td>
</tr>
</tbody>
</table>

**Example**

GET http://52.28.33.220:3000/oneapi/location/1/queries/location?requestedAccuracy=1000&address=tel%3A%2B16035558278*emphasized text*

    {
        "terminalLocationList": {
            "terminalLocation": [
                {
                    "address": "tel:+16035558278",
                    "locationRetrievalStatus": "Retrieved",
                    "errorInformation": null,
                    "currentLocation": {
                        "timestamp": "2015-05-26T09:19:43Z",
                        "altitude": 75,
                        "longitude": 2.1833333,
                        "latitude": 41.3833333,
                        "accuracy": 1000
                    }
                }
            ]
        }
    }

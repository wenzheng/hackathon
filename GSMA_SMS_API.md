**Introduction**

The authorized caller is able to send the SMS messages to one or more mobile terminals.

**URL format**

http://{serverRoot}/ericsson/oneapi/sms/1/outbound/{senderAddress}/requests/

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
<td style="text-align:left;"><p>senderAddress</p></td>
<td style="text-align:left;"><p>It is the address to which a responding SMS is sent. senderAddress in URL and payload must be same.
 </p></td>
<td style="text-align:left;"><p>Mandatory</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>message</p></td>
<td style="text-align:left;"><p> The message content which is going to be sent to the senderAddress, the length of it must be less than 160 characters
</p></td>
<td style="text-align:left;"><p>Mandatory </p></td>
</tr>
<tr>
<td style="text-align:left;"><p>clientCorrelator</p></td>
<td style="text-align:left;"><p>It uniquely identifies the request
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

Request *Post http://52.28.33.220/ericsson/oneapi/sms/1/outbound/tel%3A%2B123456789/requests*

    {"outboundSMSMessageRequest":{
     "senderAddress":"tel%3A%2B123456789",
     "outboundSMSTextMessage":{"message":"Hello World!"},
     "address":["tel%3A%2B8613500000000"],
	 "clientCorrelator": "12312",
     "receiptRequest":{
          "notifyURL":"https://example.com:7464/smsStatus",
          "callbackData":"doSomething()"
          }
     }
     }



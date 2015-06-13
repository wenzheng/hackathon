**Introduction**

The authorized caller is able to charge/refund an end user.

**URL format**

http://{serverRoot}/oneapi/payment/1/{endUserId}/transactions/amount


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
<td style="text-align:left;"><p>endUserId </p></td>
<td style="text-align:left;"><p>It is the identity of the end user to be charged. tel URI is used as the user identity. Only global number is supported.<br>"tel:" scheme must be given. For example, tel%3A%2B8613500000000<br>
The endUserId value in URL and payload must be same.
 </p></td>
<td style="text-align:left;"><p>Mandatory</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>referenceCode </p></td>
<td style="text-align:left;"><p> The message content which is going to be sent to the senderAddress, the length of it must be less than 160 characters</p></td>
<td style="text-align:left;"><p>Mandatory </p></td>
</tr>
<tr>
<td style="text-align:left;"><p>transactionOperationStatus </p></td>
<td style="text-align:left;"><p>This indicates the desired resource state. Set to ‘Charged’ to deduct money from user’s account, and set to ‘Refunded’ to refund user. </p></td>
<td style="text-align:left;"><p>Mandatory </p></td>
</tr>
<tr>
<td style="text-align:left;"><p>description </p></td>
<td style="text-align:left;"><p>It is the human-readable text to appear on the bill. Then user can easily see what they bought.
 </p></td>
<td style="text-align:left;"><p>Mandatory </p></td>
</tr>
<tr>
<td style="text-align:left;"><p>currency </p></td>
<td style="text-align:left;"><p>It is the 3-figure code as per ISO 4217.
 </p></td>
<td style="text-align:left;"><p>Mandatory </p></td>
</tr>
<tr>
<td style="text-align:left;"><p>amount </p></td>
<td style="text-align:left;"><p>It can be a whole number or decimal.
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

Example: Post: http://52.28.33.220/ericsson/oneapi/payment/1/tel:+8613580551660/transactions/amount?endUserId=tel:+8613580551660&transactionOperationStatus=Charged&description=&currency=EUR&amount=18&referenceCode=REF-1234


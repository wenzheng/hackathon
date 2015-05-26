All the attribute which is not marked as readonly from read car information API can be updated in this API.

The API format is: POST http://52.28.33.220:3000/vehicle/v2/{vin} postbody

This API is used to retrieve all car related information, the format is:

GET http://52.28.33.220:3000/vehicle/v2/{vin}

<table>
<thead>
<tr>
<th id="parameter" style="text-align:left;">Parameter            </th>
<th id="type" style="text-align:left;">Type        </th>
<th id="required" style="text-align:left;">Required   </th>
<th id="read_only" style="text-align:left;">Read only   </th>
<th id="description" style="text-align:left;">Description   </th>
</tr>
</thead>

<tbody>

<tr>
<td style="text-align:left;"><p><strong>Vehicle status</strong> </p></td>
</tr>

<tr>
<td style="text-align:left;"><p>speed </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Vehicle speed (KM/h or MP/h</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>averageSpeed </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Estimated average speed in KM/h </p></td>
</tr>

<tr>
<td style="text-align:left;"><p>rpm </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Engine RPM 10X1000.</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>fuel_usage </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Fuel level as a percentage of fullness</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>oil_life </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Remaining engine oil as percentage of fullness</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>oil_pressure </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Engine Oil Pressure in PSi</p></td>
</tr>

<tr>
<td style="text-align:left;"><p><strong>Vehicle climate control</strong> </p></td>
</tr>

<tr>
<td style="text-align:left;"><p>airflow_direction </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Airflow direction: "frontpanel", "floorduct",   "bilevel", "defrostfloor"</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>fan_speed_level </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Fan speed of the air flowing (0: off, 1: weakest ~ 10: strongest )</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>target_temperature </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Desired temperature(in degrees Celsius)</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>air_conditioning </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Air conditioning system T/F</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>heater_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Heating system T/F</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>seat_heater_state </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Seat warmer (0: off, 1: least warm ~ 10: warmest)</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>seat_cooler_state </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Seat ventilation (0: off, 1: least warm ~ 10: warmest)</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>air_recirculation </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Air recirculation. (True : on, False : pulling in outside air)</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>steeringWheelHeater </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Steering wheel heater (0: off, 1: least warm ~ 10: warmest)</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>front_left_window_lock_status</p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the window is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>front_right_window_lock_status </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the window is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>rear_right_window_lock_status </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the window is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>rear_left_window_lock_status </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the window is locked T/F</p></td>
</tr>

<tr>
<td style="text-align:left;"><p>front_right_window_openness </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Side window as a percentage of openness. (0:Closed, 100:Fully Opened)</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>rear_left_window_openness </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Side window as a percentage of openness. (0:Closed, 100:Fully Opened)</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>rear_right_window_openness </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Side window as a percentage of openness. (0:Closed, 100:Fully Opened)</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>front_left_window_openness </p></td>
<td style="text-align:left;"><p>Integer </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Side window as a percentage of openness. (0:Closed, 100:Fully Opened)</p></td>
</tr>

<tr>
<td style="text-align:left;"><p><strong>Driving safety</strong> </p></td>
</tr>

<tr>
<td style="text-align:left;"><p>driver_door_state </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Door status enum: "open", "ajar", "close"</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>hood_door_state </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Door status enum: "open", "ajar", "close"</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>rear_left_door_state </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Door status enum: "open", "ajar", "close"</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>fuel_door_state </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Door status enum: "open", "ajar", "close"</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>trunk_door_state </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Door status enum: "open", "ajar", "close"</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>passenger_door_state </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Door status enum: "open", "ajar", "close"</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>rear_right_door_state </p></td>
<td style="text-align:left;"><p>String </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Door status enum: "open", "ajar", "close"</p></td>
</tr>


<tr>
<td style="text-align:left;"><p>rear_right_door_lock_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the door is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>rear_left_door_lock_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the door is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>driver_door_lock_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the door is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>hood_door_lock_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the door is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>passenger_door_lock_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the door is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>fuel_door_lock_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the door is locked T/F</p></td>
</tr>
<tr>
<td style="text-align:left;"><p>trunk_door_lock_state </p></td>
<td style="text-align:left;"><p>Boolean </p></td>
<td style="text-align:left;"><p>False </p></td>
<td style="text-align:left;"><p>No </p></td>
<td style="text-align:left;"><p>Whether or not the door is locked T/F</p></td>
</tr>

</tbody>
</table>

Below is an example that how to  control the air flow direction

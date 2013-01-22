12-Servo BoosterPack for Stellaris Launchpad
============================================
by KROESCHE.ORG

---

License
-------
All documentation and design files including schematic and board layout is licensed under a Creative Commons Attribution 3.0 Unported License.

You should have received a copy of the license along with this work.  If not, see <http://creativecommons.org/licenses/by/3.0/>.

Please see the accompanying file LICENSE.TXT.

Summary
-------
This board is designed to be used with a Stellaris Launchpad.  It provides a power supply and connectors for 12 servos.  Each servo control signal can be driven from one half of a Stellaris Wide Timer.  The board is intended to be powered from a 2-cell LiPo battery pack and it will provide a 5-volt supply for the servos and optionally the Launchpad.

Power Supply
------------
The board is intended to be powered from a 2-cell LiPo battery pack or similar and can tolerate an input range of about 6-12V.  The onboard power supply will produce 5 volts with a current up to 5 amps.  The onboard supply can also be used to power the Stellaris Launchpad that is plugged in to the servo board. In order to do this, the jumper JP1 must be shorted.  By leaving this jumper open, you can choose to power the launchpad from a separate supply, either at J10 or through the Launchpad USB connector.

Battery Voltage Measurement
---------------------------
There is a circuit to allow for measurement of the battery supply voltage using the Stellaris A/D convertor.  It uses analog input signal AIN2.  It is scaled so that 3V supply reads 0 and 4.5V supply reads full scale.

Connectors
----------
* X1 - battery power supply, 6-12 V
* S0A - servo connector, uses wide timer 0A
* S0B - servo connector, uses wide timer 0B
* SnA/B - remaining servo connectors, using wide timer nA/B
* JP1 - short this jumper to supply Launchpad from the onboard supply
* J10 - can supply Launchpad 5V here if JP1 is left open
* J1-J4 - standard Launchpad connectors
* J5 - additional non-standard Launchpad connector needed for wide timer 4

Notes
-----
* If you want to use wide timer 4 (and you will if you want all 12 servos), you will need to add a stake-header connector to your Launchpad in the two holes next to the USB device connector.  You will not be able to use the USB device function if you use wide timer 4 for servo control.

* The board is intended to go under the Launchpad (LP sits on top), but there is no reason that it could not also plug on top of a LP.  It might cover some of the buttons on the top.

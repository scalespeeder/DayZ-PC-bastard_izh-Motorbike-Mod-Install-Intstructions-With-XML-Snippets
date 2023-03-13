DayZ Chernarus & Livonia PC "bastard_izh" Motorbike & Sidecar Mod by  bastard.info PC Install Instructions & Terms Of Use

Many thanks to  bastard.info for creating this amazing mod. Please visit his website, bastard.info

THIS IS AN EARLY SET OF FILES COMPRISED OF BASTARD.INFO'S FILE FROM HIS STEAM PAGE & MY ADDITIONS, SO SERVER OWNERS CAN EASILY SPAWN IN MOTORBIKES WITHOUT USING ADMIN TOOLS OR TRADER.
THESE FILES WILL PROBABLY BE SUPERCEDED AS BASTARD.INFO ADDS TO HIS OWN XMLS.

Spawns four types of motorcycles with sidecars at various points around Chernarus and Livonia.(See photos in Github)

Motorbikes will be complete, you just need to add fuel (which is stored in the cargo.)

THIS IS NOT bastard.info's OFFICIAL INSTALL INSTRUCTIONS AND IS NOT AFFILIATED WITH bastard.info

Limited Testing on PC Chernarus & Livonia Local Server & Nitrado Community PC Server DAYZ Version 1.20 Mar 2023.

XML snippets Created by @scalespeeder & bastard.info. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

PLEASE SEE THE STEAM PAGE OF THE MOD FOR TERMS OF USE: https://steamcommunity.com/sharedfiles/filedetails/?id=2944122126

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Subscribe to bastard_izh on Steam:

https://steamcommunity.com/sharedfiles/filedetails/?id=2944122126

& cf

https://steamcommunity.com/workshop/filedetails/?id=1559212036

& survivor animations

https://steamcommunity.com/workshop/filedetails/?id=2918418331

& bastard_framework

https://steamcommunity.com/workshop/filedetails/?id=2920006107

Start your DayZ Launcher to download the mod files. Using your FTP programme, copy the @bastard_izh , @CF , @Survivor Animations & @bastard_framework folders from your DayZ !workshop folder
to the root directory of your server. Copy the keys from the mods key folder to your servers key folder. Edit your start batch file,
so that your server will load @bastard_izh , @CF , Survivor Animations & @bastard_framework mods on startup. (On Nitrado and some other DayZ Server Providers you don't have access to the batch file,
instead you will find an "Additional mods" setting in the settings section of your servers web interface, add @bastard_izh there. It should look soomething like this: @CF;@bastard_framework;@Survivor Animations;@bastard_izh )


Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access. All the xml snippets you need are within this readme.

Stop your server using it's web control panel.

Using FTP or your Servers file browser, make the following additions to your XMLS:

Open your events.xml file (its in the db folder on your server) and add the following XML snippet at the top, below the <events> tag:

<!-- bastard_izh motorbike events additions-->

<event name="Vehiclebastard_izh">
<nominal>8</nominal>
<min>7</min>
<max>8</max>
<lifetime>300</lifetime>
<restock>0</restock>
<saferadius>500</saferadius>
<distanceradius>500</distanceradius>
<cleanupradius>200</cleanupradius>
<flags deletable="0" init_random="0" remove_damaged="1"/>
<position>fixed</position>
<limit>mixed</limit>
<active>1</active>
<children>
<child lootmax="0" lootmin="0" max="2" min="2" type="bastard_izh_stock"/>
<child lootmax="0" lootmin="0" max="2" min="2" type="bastard_izh_blue"/>
<child lootmax="0" lootmin="0" max="2" min="2" type="bastard_izh_black"/>
<child lootmax="0" lootmin="0" max="2" min="2" type="bastard_izh_white"/>
</children>
</event>
	
<!-- end of bastard_izh motorbike events additions -->


Open your types.xml file (its in the db folder on your server) and add the following XML snippet at the top, below the <types> tag:

<!-- bastard_izh motorbike types additions-->

  <type name="bastard_izh_stock">
<nominal>0</nominal>
<lifetime>3888000</lifetime>
<restock>0</restock>
<min>0</min>
<quantmin>100</quantmin>
<quantmax>100</quantmax>
<cost>100</cost>
<flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0"/>
</type>

<type name="bastard_izh_blue">
<nominal>0</nominal>
<lifetime>3888000</lifetime>
<restock>0</restock>
<min>0</min>
<quantmin>100</quantmin>
<quantmax>100</quantmax>
<cost>100</cost>
<flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0"/>
</type>

<type name="bastard_izh_white">
<nominal>0</nominal>
<lifetime>3888000</lifetime>
<restock>0</restock>
<min>0</min>
<quantmin>100</quantmin>
<quantmax>100</quantmax>
<cost>100</cost>
<flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0"/>
</type>

<type name="bastard_izh_black">
<nominal>0</nominal>
<lifetime>3888000</lifetime>
<restock>0</restock>
<min>0</min>
<quantmin>100</quantmin>
<quantmax>100</quantmax>
<cost>100</cost>
<flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0"/>
</type>

<type name="bastard_izh_Wheel_Ruined">
<nominal>0</nominal>
<lifetime>7200</lifetime>
<restock>0</restock>
<min>0</min>
<quantmin>100</quantmin>
<quantmax>100</quantmax>
<cost>100</cost>
<flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="1" deloot="0"/>
<category name="vehiclesparts"/>
</type>

<type name="bastard_izh_Wheel">
<nominal>20</nominal>
<lifetime>28800</lifetime>
<restock>0</restock>
<min>20</min>
<quantmin>100</quantmin>
<quantmax>100</quantmax>
<cost>100</cost>
<flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0"/>
<category name="vehiclesparts"/>
<usage name="Industrial"/>
<usage name="Farm"/>
</type>
	
<!-- end of bastard_izh motorbike types additions-->
	
Save the file and re-upload if necessary.

Open your cfgspawnabletypes.xml file (its in the root folder of the mission folder on your server) and add the following XML snippet,
just below <spawnabletypes> which is near the top of the file:

<!-- start of bastard_izh motorbike spawnabletypes -->
	
<type name="bastard_izh_stock">
<damage min="0.0" max="0.0" />
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="SparkPlug" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CarBattery" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="HeadlightH7" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CanisterGasoline" chance="1.00" />
</attachments>
</type>

<type name="bastard_izh_blue">
<damage min="0.0" max="0.0" />
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="SparkPlug" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CarBattery" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="HeadlightH7" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CanisterGasoline" chance="1.00" />
</attachments>
</type>

<type name="bastard_izh_white">
<damage min="0.0" max="0.0" />
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="SparkPlug" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CarBattery" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="HeadlightH7" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CanisterGasoline" chance="1.00" />
</attachments>
</type>

<type name="bastard_izh_black">
<damage min="0.0" max="0.0" />
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="bastard_izh_Wheel" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="SparkPlug" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CarBattery" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="HeadlightH7" chance="1.00" />
</attachments>
<attachments chance="1.00">
<item name="CanisterGasoline" chance="1.00" />
</attachments>
</type>
	
<!--end of bastard_izh motorbike spawnabletypes additions-->
	
	
	Open your CHERNARUS cfgeventspawns.xml file (its in the root folder of the mission folder on your server) and add the following XML snippet,
just below <eventposdef> which is near the top of the file:
	
<!-- bastard_izh motorbike CHERNARUS event spawns additions-->
	
<event name="Vehiclebastard_izh">
		<pos x="5834.00" z="2436.45" a="1.736423" /> 
		<pos x="10248.99" z="3187.92" a="1.736423" />
		<pos x="12781.77" z="4451.40" a="32.092476" />
		<pos x="12048.09" z="9274.13" a="-36.527287" />
		<pos x="13323.47" z="12880.15" a="100.383453" />
		<pos x="7521.06" z="8296.69" a="0.000000" /> 
		<pos x="2963.42" z="6631.07" a="-13.206916" />
		<pos x="7347.55" z="11214.23" a="-142.020447" />
		</event>
	
<!-- end of bastard_izh motorbike CHERNARUS event spawns additions -->

	Open your LIVONIA cfgeventspawns.xml file (its in the root folder of the mission folder on your server) and add the following XML snippet,
just below <eventposdef> which is near the top of the file:

<!-- bastard_izh motorbike LIVONIA event spawns additions-->

<event name="Vehiclebastard_izh">
		<pos x="944.14" z="5582.58" a="1.736423" />
		<pos x="1435.16 " z="9547.58" a="1.736423" />
		<pos x="6161.72" z="11261.64" a="32.092476" /> 
		<pos x="8884.77" z="10074.96" a="-36.527287" />
		<pos x="11672.07" z="8378.87" a="100.383453" /> 
		<pos x="8682.42" z="6660.70" a="0.000000" /> 
		<pos x="5929.10" z="7404.26" a="-13.206916" /> 
		<pos x="11178.13" z="791.56" a="-142.020447" />
		</event>
	
<!-- end of bastard_izh motorbike LIVONIA event spawns additions -->

Save your changes & upload if you need to.

Restart your server and the motorbikes will be spawning in for the enjoyment of your players!!!!!

Thanks again to bastard.INFO (!!!!)

Thanks, Rob.

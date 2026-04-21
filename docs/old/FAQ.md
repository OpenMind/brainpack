# Frequently Asked Questions

## Overheating & Fire Risk

### Is there a risk of overheating if it runs for hours?
Running the backpack for hours over multiple charge cycles does not cause overheating.

### What safety cut-offs exist to prevent battery fires?
In case of high temperatures, the on-board computer (Jetson AGX) automatically shuts off to prevent damage to electronics. 


## Battery & Charging

### How long does it take to fully charge, and is it safe to leave charging overnight?
Should be safe to leave on charging. Auto charging should disable when fully charged, but we're still developing this feature.

### Can I use any charger, or do I need a special one?
Should use only the provided charge stations or seller approved alternatives (eg. from unitree)

### What happens if the battery gets damaged (dropped, punctured)?
If the battery is visibly damaged, broken or non-functioning, please contact Unitree. A replacement will be necessary.

## Children & Pets

### Is it safe to have this running around small kids?
Completely safe.

### Are there safeguards to prevent sudden, jerky movements?
Yes, there are separate movement algorithms by Openmind and Unitree that handle this. Sudden jerky movements are unlikely unless 2 or more feet are not touching the ground at any given moment.

## Physical Safety

### Are there sharp edges, pinch points, or exposed parts?
No sharp edges or pinch points, but it is strongly recommended to avoid touching the backpack and (especially) the sensors like the lidar after prolonged usage.

### What happens if it bumps into furniture — could it damage walls or itself?
Unlikely unless at high speeds or with great force.

### Can it climb stairs safely without falling?
Not at the moment.

## Reliability & Control

### What if the Wi-Fi drops — does the dog freeze, shut down, or keep moving?
If disconnected from the WiFi, the dog will stay in its last recorded valid state (current position). In this case, you may connect to the dog using your phone through the Unitree App and RC it to within connectivity range.

### Is there an emergency stop button or voice command?
E-Stop exists within the Unitree app that shuts down all motors instantly. Additionally, pressing 'B' on the controller will make it stop motion.

### What’s the backup if the AI misunderstands a command?
There is an inbuilt governance model that evaluates commands to make sure they are not misunderstood, the AI is expected to only respond and perform actions within its governance. In case of ambiguity, the AI is expected to query and ask for more information. In case of a violation of its governance, the AI is expected to comply only as far as its governance allows.

## Privacy & Recording

### Is the dog always recording audio/video in my home?
There is an opt-in feature that enables/disables audio and video processing capabilities. Video data is not recorded.

### Where does that data go — cloud or local storage?
Only a live video recording is displayed, it is not stored locally or in the cloud. 

### Can I turn off cameras/mics easily?
You cannot turn off the camera/mic individually, you must turn off the whole system. OM1 will automatically blur faces as a privacy feature. 


## Durability

### How well does it handle drops, spills, or someone tripping over it?
The robot dog can maintain its own balance. Dropping or application of force may damage the electronics or internal components of the dog backpack. It is recommended to avoid any commands that might lead to the robot tilting excessively.

### What’s the expected lifespan of the battery and backpack?
Battery should last 3-4 hours on a single charge, without auto charging

### How weather-proof is it (rain, outdoor use)?
Not waterproof (as of yet) and not intended for inclement weather or rugged outdoor conditions.

## Costs & Maintenance

### How expensive are replacement batteries or repairs if something goes wrong?
Replacement batteries generally cost upwards of $660. In case of any issues with electronics, the robot dog will need to be sent for repairs.

### How often do I need to update software or do maintenance?
OM1 functionality is automatically kept up to date. There is no manual software updates or maintenance required. 

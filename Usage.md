**A simple yet pleasant looking Watchy Face, loaded with features**


![Watchy GSR Face](https://github.com/GuruSR/Watchy_GSR/blob/main/Watchy_GSR.jpg)

This Watchy "face" contains the following heiarchy of options and settings:

**Legend**:  **{}** items are defaults.

|Menu | Sub-Menu Item | Function Description |
|---- | ------------- | -------------------- |
|**Steps** | Reset Time        | Reset Steps ... Use Menu information for more help. |
|**Alarms** | Alarms #         |  HH:MM -> Full -> Days + Repeat + Active settings |
|           | Tone Repeats     |  **{Full}** repeats.  Allows you to reduce the amount of alarm tones that repeat (80%-20% in 20% increments).  Resets the tone repeats for all alarms when you change this. |
|**Timers** | Countdown Timer  | HH:MM -> {Full} -> On/**{Off}**  (Full, see Tone Repeats above for information). |
|           | Elapsed Time     | HH:MM On/**{Off}** |
|**Options** | Display Style   | **{Light}** or Dark mode. |
|            | Border Mode     | Border around the display:  **{Show}** (White) or Hide (Black). |
|            | Dexterity       | Swap the Back/Menu with UP/DOWN for left-handed users. |
|            | Menu & Back     | **{Normal}** or Swap the Menu & Back button positions. |
|            | Orientation     | Ignore button on Watchy orientation:  **{Ignore}** or Watchy UP. |
|            | Time Mode       | **{AM/PM}** or 24 Hour mode of time display. |
|            | Feedback        | **{Enable}** or Disable haptic feedback on button presses (during use). |
|            | Turbo Time      | How many seconds Watchy stays active after your last button press before sleeping. |
|            | Reset Screen    | Reset screen if artifacting or ghosting is happening. |
|            | Sync Watchy     | Sync Watchy RTC by Time, TimeZone, TimeZone & Time |
|            | Watchy Connect  | Used to give the WiFi "X" credentials to Watchy.  "X" WiFi is the last "good" connected WiFi. |
|            | OTA Update      | Used with Arduino (and platformio) to upload a compile to Watchy via WiFi.  (ESCAPE by holding "BACK" for 10 seconds.) |
|            | OTA Website     | Website offers Backup & Restore of Settings, WiFi AP Settings and WiFi OTA upload of a bin file.  (ESCAPE by holding "BACK" for 10 seconds.) |
|            | Watchy Reboot   | Reboot the Watchy in the event something stops working. |
            
Button usage:

- "Menu" (SW1):  Activates/Toggles items, for Alarms, Timers and Step, advances forward where HH:MM is shown.  In Turbo Time increases seconds.
- "Back" (SW2):  Backs out of an item or backs up to previous section when in HH:MM areas.
-  "UP"  (SW3):  Moves menu selection up.  When inside HH:MM it increases selected value (these cycle if above max value).
- "DOWN" (SW4):  Moves menu selection down.  When inside HH:MM it decrease selected value (these also cycle if below 0).

STEPS:

- Steps holds the current steps and (Yesterday's steps if any).
- Reset Time (HH:MM) represents the time of day where the Step counter is automatically reset and placed in the "Yesterday"'s list.
- Reset Steps will reset the current steps but will *NOT* move them to "Yesterday".

ALARMS:  (WHITE settings means "ON", Black is "OFF")

- Alarms allow HH:MM setting
- Tone Repeats are custom per Alarm but are reset to the value you use in Tone Repeats.
- All days of the week can be toggled On/**{Off}**.  White days are the only active days.
- Repeat offers to repeat the choices.  If Repeat is **{off}**, day will go Black.
- Active sets the alarm as operational or **{not}**.

TIMERS:

- Countdown Timer will count down from the HH:MM you set.  On/Off will reset the HH:MM when pressed.
- Elapsed Timer will count up when started (On) and will stop **{Off}** when stopped.  Starting again resets to 00:00.

ALARMS & COUNTDOWN TIMER PULSES:

- ALARM TONES:
  1.  Large solid pulse.  (LOUD)
  2.  2 smaller pulses.   (NOISY)
  3.  3 tiny pulses.  (QUIET)
  4.  2 very tiny pulses, a very tiny pause, 2 more very tiny pulses.  (VERY QUIET, useful in meetings)

- COUNTDOWN:  6 very tiny pulses.

These will cycle in a loop from ALARM 1 to COUNTDOWN playing their tones until they run out.  All 5 will not last longer than 50 seconds.  To stop them from playing, edit their time.  Each Alarm (and the Countdown Timer) have their own reduction for repeats of their tones, which will shorten these durations.

FIRST TIME USAGE:

1.  Go into Options -> Watchy Connect -> MENU to Connect.
2.  Connect to the Watchy Connect WiFi access point with your phone, laptop, computer, etc.  (Password is:  Watchy123)
3.  Scan for your home network (or whichever one you want to use it with) and setup the WiFi connectivity there, once it works, the Access Point will close.  This will ALWAYS ask for a new WiFi setting, unlike previous versions, you can change your WiFi "X" (last known good connection).
4.  Go to (Options -> ) OTA Website, browse to the IP address in Watchy menu.
5.  Pick "Backup & Restore Settings" to restore your previous Watchy settings, paste in the settings you had and click Store.

WiFi USAGE:

WiFi now has 10 entries (AP A to AP J), the most recent successfully connected AP is labelled "X".  See compilation for usage for making a default "X".

WiFi entries can be edited from Watchy's Options -> OTA Website, surf to the Watchy in a browser and select "Edit Additional WiFi Access Points".  When they are correct, click "Store".  The "?" at the end of each password, lets you toggle the *'s on/off.
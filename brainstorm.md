# Data model
    
    {
        "name" : "A unique name for this sysex dump"
        "createdAt" : "2014-06-25T00:00:00.000Z",
        "updatedAt" : "2014-06-25T00:00:00.000Z",
        "createdBy" : "john.doe@example.com",
        "updatedBy" : "john.doe@example.com",
        "rating" : 3,
        "manufacturer" : [0x00, 0x20, 0x29],
        "device" : "Bass Station II",
        "data" : [0xF0, ..., 0xF7]
    }

### MIDI Manufacturer ID

- https://www.midi.org/specifications/item/manufacturer-id-numbers
- http://www.amei.or.jp/report/System_ID_e.html

Midi device ID:

- https://github.com/jazz-soft/JZZ-midi-Gear/blob/master/data/models.txt

# Features

- Receive SysEx 
- Send SysEx
- Save SysEx (in local storage)
- Export SysEx as file (Save As...)
- Load SysEx from file (Open File...)
- Share as unique URL (SysEx data urlencoded in query-string)
- Choose MIDI channel
- Allow for multiple devices to be connected at the same time
- Auto-detect manufacturer from ID
- Sort list
    - tag, device, manufacturer, date, author, rating 
- Filter list
    - free-form filter
- Organize
    - Tags
    - Folders?    
- Bulk export (as zip file)
- Bulk import (select files...)    
    
## Data Storage

- Everything is stored client-side
- By default, no communication with SysEx.io at all

- HTML5 file API ? http://html5-demos.appspot.com/static/html5storage/index.html#slide45
    - NO, not enough support yet
    
### Cloud storage with zero-knowledge

- http://slides.com/jjperezaguinaga/zero-knowledge-solutions-with-javascript#/
- https://softwareengineering.stackexchange.com/questions/262118/how-to-implement-simple-secure-client-side-encryption
- https://github.com/heartnotes/heartnotes
- https://github.com/bitwiseshiftleft/sjcl
- https://github.com/SpiderOak/crypton


### Feature to add:

- Share your dump with SysEx.io to allow updating of the Device Model ID big list. 
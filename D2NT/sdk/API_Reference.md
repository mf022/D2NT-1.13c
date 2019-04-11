## Other Info Sources
- [D2NT] API Reference by Muddy Waters - http://www.elitepvpers.com/forum/diablo-2-programming/1069225-d2nt-api-reference-no-questions.html
- some references for D2BS - https://github.com/noah-/d2bs 

## Global Functions 

CheckCollision()

ClickMap()

CloseD2()

Delay()

ExitGame()


### FileOpen()

* Syntax:

filehandle = FileOpen(string path, int mode);

* Description:

Returns File object handle for the file at the specified path.

* Parameter:

Possible values for mode:
0 - Read
1 - Overwrite
2 - Append/Read

* Return Value(s):


* Notes:

Returns null if the file could not be opened.
The path is relative. The root is the scripts folder.

* Example:

// Open a File "MyTest.txt" in the scripts folder
// create it if it doesn't exist
var _fhandle = FileOpen("MyTest.txt", 1);
if(_fhandle)
{
    // Write a line, overwriting the file's previous content
    _fhandle.WriteLine("My foo file");
    _fhandle.Close(); // Close the file handle
}

### GetArea()

* Syntax:

[1] Area GetArea(void);
[2] Area GetArea(int areaid);

* Description:

Returns File object handle for the file at the specified path.

* Parameter:

[1] Returns an Area object according to your char's current whereabouts.
[2] Returns an Area object according to the areaid specified.
Possible values of area ID: - ...\sdk\areas.txt

* Return Value(s):


* Notes:

Raises an unhandled exception when called using invalid arguments.

* Example:



GetBaseStat()

GetControl()

GetCursorType()

GetDistance()


### GetLocaleString()
- GetLocaleString Contains too much information to be shown directly 

GetPath()

GetPlayerFlag()

GetPlayerUnit()

GetPresetUnits()

GetRoom()

GetScript()

GetTickCount()

GetUIState()

GetUnit()

GetWaypoint()

Gold()

Include()

Load()

Print()

RegisterEvent()

Random()

RunGC()

Say()

SendCopyData()

SetStatusText()

SetUIState()

SubmitItem()

Transmute()

UnregisterEvent()


## Me (Global Object)

### Me.Account

* Syntax:

me.account

* Description:

A core variable that contains the account name of the current profile being used.

* Parameter:

nil

* Return Value(s):

String <account name>

* Notes:


* Example:

[div] style="border: 1px dotted grey; width: 400px; padding: 5px"
| controlData.setText(controlData.controls.login.editBox.accountName, me.account);

enters the account name during login.

### Me.Act

* Syntax:

me.act

* Description:

The act where the controlled unit is currently located.

* Parameter:

nil

* Return Value(s):

Int <current act>
Possible values 1 to 5

* Notes:


* Example:

#### 
if(me.act == 2){
//<do an action>
}

### Me.Areaid

* Syntax:

me.areaid

* Description:

The id of the area where the controlled unit is currently located.

* Parameter:

nil

* Return Value(s):

Int <current area>
Possible values: - ...\sdk\areas.txt

* Notes:


* Example:

[div] style="border: 1px dotted grey; width: 400px; padding: 5px"
| Print("I am currently in area " + me.areaid);

### Me.Charloc

* Syntax:

int me::charloc;

* Description:

The controlled unit's zero based position on the account.
Account Layout:
[0] [1]
[2] [3]
[4] [5]
[6] [7]

* Parameter:


* Return Value(s):


* Notes:

This value equals the positions that is selected in the characters profile less one.

* Example:

### Me.Charname

* Syntax:

String me::charname;

* Description:


* Parameter:

The name of the controlled unit.

* Return Value(s):


* Notes:

Identical to the Global Object, me.name

* Example:

### Me.Chickenhp

* Syntax:

int me::chickenhp;

* Description:

The chicken threshold for the controlled unit.
If your hit points drop below this value, your character will leave the game.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Chickenmp

* Syntax:

int me::chickenmp

* Description:

The chicken threshold for the controlled unit.
If your mana points drop below this value, your character will leave the game.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Classid

* Syntax:

int me::classid;

* Description:

The classid represents the character class of the controlled unit.
Possible values:- ...\sdk\classid.txt

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Diff

* Syntax:

int me::diff;

* Description:

The difficulty of the game the character is currently in.
Possible values:
0 - Normal
1 - Nightmare
2 - Hell

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Gamename

* Syntax:

String me::gamename;

* Description:

The name of the game the character is currently in.

* Parameter:


* Return Value(s):


* Notes:

After leaving the current game, this value will still hold the name of the game that was just left.
It is not refreshed until the character joins another game.

* Example:

### Me.Gamepassword

* Syntax:

String me::gamepassword;

* Description:

The password of the game the character is currently in.

* Parameter:


* Return Value(s):


* Notes:

After leaving the current game, this value will still hold the password of the game that was just left.
It is not refreshed until the character joins another game.

* Example:

### Me.Gameserverip

* Syntax:

String me::gameserverip;

* Description:

The IP adress of the current game server.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Gametype

* Syntax:

int me::gametype;

* Description:

The game type of the controlled unit.
Possible values:
0 - Classic
1 - Expansion

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Gatewayid

* Syntax:

int me::gatewayid;

* Description:

The ID of your gateway as selected in profile.
Possible Values:
0 - U.S. West
1 - U.S. East
2 - Asia
3 - Europe

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Gid

* Syntax:

int me::gid;

* Description:

The controlled unit's ID which is unique within a single game.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Hpmax

* Syntax:

int me::hpmax;

* Description:

The maximum number of hit points that the controlled unit can currently have.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Hp

* Syntax:

int me::hp;

* Description:

The number of hit points that the controlled unit currently has.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Ingame

* Syntax:

bool me::ingame;

* Description:

Whether or not the controlled unit is currently in a game.

* Parameter:


* Return Value(s):


* Notes:


* Example:

Me.itemoncursor

### Me.Ladder

* Syntax:

bool me::ladder;

* Description:

Whether or not the controlled unit is a ladder character.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Maxgametime

* Syntax:

int me::maxgametime;

* Description:

The maximum number of seconds for which the controlled unit stays in a single game.

* Parameter:


* Return Value(s):


* Notes:

If the actual gametime exceeds the maximum gametime, the controlled unit will exit the game.
Set to 0 never to leave a game.

* Example:

### Me.Mode

* Syntax:

int me::mode;

* Description:


The mode of the controlled unit.

Possible Values: - ...\sdk\modes.txt

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Mpmax

* Syntax:

int me::mpmax;

* Description:

The maximum number of mana points that the controlled unit can currently have.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Mp

* Syntax:

int me::mp;

* Description:

The number of mana points that the controlled unit currently has.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Name

* Syntax:

String me::name;

* Description:

The name of the controlled unit.

* Parameter:


* Return Value(s):


* Notes:

Identical to global object, me.charname

* Example:

### Me.Ping

* Syntax:

int me::ping;

* Description:

Your current ping in ms.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Playertype

* Syntax:

bool me::playertype;

* Description:

Whether or not the controlled unit is a hardcore character.

* Parameter:


* Return Value(s):


* Notes:


* Example:

Me.Playtype

### Me.Quitonhostile

* Syntax:

bool me::quitonhostile;

* Description:

Whether or not the controlled unit is supposed to exit the game when another player expresses hostility.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Realm

* Syntax:

String me::realm;

* Description:

The name of the realm that the controlled unit is currently logged onto.
Possible Values:
"USWest"
"USEast"
"Asia"
"Europe"

* Parameter:


* Return Value(s):


* Notes:

Identical to global object, me.realmshort.

* Example:

### Me.Realmshort

* Syntax:

String me::realmshort;

* Description:

The name of the realm that the controlled unit is currently logged onto.
Possible Values:
"USWest"
"USEast"
"Asia"
"Europe"

* Parameter:


* Return Value(s):


* Notes:

Identical to global object, me.realm.

* Example:

### Me.Revealautomap

* Syntax:

bool me::revealautomap;

* Description:

Whether or not the automap is revealed.

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Runwalk

* Syntax:

int me::runwalk;

* Description:

Represents the status of the always run toggle.
Possible values:
0 - Walk
1 - Always run

* Parameter:


* Return Value(s):


* Notes:


* Example:

Me.Showenemyonautomap

Me.Showmissileonautomap

### Me.Screensize

* Syntax:

int me::screensize;

* Description:

Represents the current screensize.
Possible values:
0 - 640x480
2 - 800x600

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.Type

* Syntax:

int me::type;

* Description:

The unit type of the controlled unit.

* Parameter:


* Return Value(s):


* Notes:

Can be treated as constant, because the unit type of me is always 0 (Player).

* Example:

### Me.Weaponstab

* Syntax:

int me::weaponstab;

* Description:

The ID of the Slot currently selected.
Possible values:
0 - Slot I
1 - Slot II

* Parameter:


* Return Value(s):


* Notes:


* Example:

### Me.X

* Syntax:

int me::x;

* Description:

The x-coordinate of the controlled unit's current position.

* Parameter:


* Return Value(s):


* Notes:


* Example:

####  Print("My current position is (" + me.x + "|" + me.y + ")");


### Me.Y

* Syntax:

int me::y;

* Description:

The y-coordinate of the controlled unit's current position.

* Parameter:


* Return Value(s):


* Notes:


* Example:

####  Print("My current position is (" + me.x + "|" + me.y + ")");


### Me.Cancel()

* Syntax:

me.Cancel(int mode);

* Description:

Cancels dialogs and interactions.
mode
0 - Cancel all interactions
1 - Cancel current interaction

* Parameter:


* Return Value(s):

Bool <true/false>

* Notes:


* Example:

####  SetUIState(0x01, true); // Open inventory
me.Cancel(1); // Close inventory


### Me.ClickItem()

* Syntax:

[1] bool me::ClickItem(int mode, Unit item);
[2] bool me::ClickItem(int mode, int x, int y, int loc);
[3] bool me::ClickItem(int itemloc);

* Description:

Clicks on an item at a given location.
mode
0 - Left Click
1 - Right Click
2 - Left Click + Shift
3 - Right Click + Shift
item
The item Unit to click on.
x
The x-coordinate at the specified location.
y
The y-coordinate at the specified location.
loc
The location of the item.
0 - Inventory
2 - Trade Window
3 - Cube
4 - Stash
5 - Belt
itemloc
The location of an equipped item.
1 - Head
2 - Neck
3 - Torso
4 - Left Weapon
5 - Right Weapon
6 - Left Ring
7 - Right Ring
8 - Belt
9 - Feet
10 - Hands

* Parameter:


* Return Value(s):


* Notes:

Overloading [2] will only work, if me.itemoncursor is true.

* Example:

[div] style="border: 1px dotted grey; width: 450px; padding: 5px"
| // Pick up our armor
SetUIState(0x01, true); // Open inventory
me.ClickItem(3); // Click on our armor

// Pick up our cube and place it somewhere else (assuming the cube is in our inventory and there is sufficient room at the target position)
var i;
var _cube = me.GetItems(549);
SetUIState(0x01, true); // Open inventory

if(_cube.length > 0 && _cube[0])
{
    for(i = 0; i < 5; i++)
    {
        me.ClickItem(0, _cube[0]); // Left click on our cube

        Delay(500);

        if(me.itemoncursor)
            break;
    }
}
if(i < 5)
{
    for(i = 0; i < 5; i++)
    {
        me.ClickItem(0, 0, 0, 0); // Left click at the upper left corner of our inventory

        Delay(500);

        if(!me.itemoncursor)
            break;
    }
}

Me.ClickMercItem()

Me.ClickParty()

Me.GetCursorItem()

Me.GetMercCost()

Me.GetQuest()

Me.GetSkillStatus()

Me.Repair()

Me.SelectNPCMenu()

### Me.SetSkill()

* Syntax:

bool Me.SetSkill(int skillid, int hand);

* Description:

skillid = Id of skill to set.
hand = 0 (Right) / 1 (Left)

* Parameter:


* Return Value(s):


* Notes:


* Example:

Me.SwapWeapons()

Me.TakeWaypoint()

Me.UseBelt()


## Unit 

Unit.act

Unit.areaid

Unit.classid

Unit.code

Unit.gid

Unit.hp

Unit.hpmax

Unit.itemclass

Unit.itemdesc

Unit.itemflag

Unit.itemlevel

Unit.itemloc

Unit.itemprefix

Unit.itemsuffix

Unit.itemtype

Unit.mode

Unit.mp

Unit.mpmax

Unit.name

Unit.quality

Unit.shrinetype

Unit.spectype

Unit.subareaid

Unit.type

Unit.x

Unit.xsize

Unit.y

Unit.ysize

Unit.GetItemCost()

Unit.GetItems()

Unit.GetMerc()

Unit.GetNext()

Unit.GetOptimalAttackPos()

Unit.GetParent()

Unit.GetRoom()

Unit.GetSkill()

Unit.GetStat()

Unit.GetState()

Unit.IsAttackable()


## Script

Script.name

Script.gametype

Script.running

Script.GetNext()

Script.Send()

Script.Stop()


## PlayerUnit

PlayerUnit.areaid

PlayerUnit.classid

PlayerUnit.gid

PlayerUnit.level

PlayerUnit.life

PlayerUnit.name

PlayerUnit.partyflag

PlayerUnit.partyid

PlayerUnit.x

PlayerUnit.y

PlayerUnit.GetNext()


## PresetUnit

PresetUnit.areaid

PresetUnit.type

PresetUnit.id

PresetUnit.x

PresetUnit.y

PresetUnit.roomx

PresetUnit.roomy

PresetUnit.subareaid


## File

File.eof

File.pos

File.size

File.Close()

File.ReadLine()

File.WriteLine()


## Control

Control.disabled

Control.pressed

Control.text

Control.type

Control.x

Control.xsize

Control.y

Control.ysize

Control.Click()

Control.GetNext()

Control.GetText()

Control.SetText()


## Area

### Area.id


* Syntax:

int Area::id;

* Description:

The ID of the area that is represented by this object.

* Parameter:

Possible values of area ID: - ...\sdk\areas.txt

* Return Value(s):



* Notes:



* Example:

### Area.name


* Syntax:

String Area::name;

* Description:

The localized name of the area that is represented by this object.

* Parameter:



* Return Value(s):



* Notes:



* Example:

### Area.x


* Syntax:

int Area::x;

* Description:

The x-coordinate of the area's origin (smallest x).

* Parameter:



* Return Value(s):



* Notes:

Multiply this value by 5 to get the area's actual x-coordinate.

* Example:

### Area.xsize


* Syntax:

int Area::xsize;

* Description:

The area's length in x-direction (width).

* Parameter:



* Return Value(s):



* Notes:

Multiply this value by 5 to get the area's actual width.

* Example:

### Area.y


* Syntax:

int Area::y;

* Description:

The y-coordinate of the area's origin (smallest y).

* Parameter:



* Return Value(s):



* Notes:

Multiply this value by 5 to get the area's actual y-coordinate.

* Example:

### Area.ysize


* Syntax:

int Area::ysize;

* Description:

The area's length in y-direction (height).

* Parameter:



* Return Value(s):



* Notes:

Multiply this value by 5 to get the area's actual height.

* Example:


## Room


Room.areaid

Room.correcttomb

Room.x

Room.xsize

Room.y

Room.ysize

Room.GetFirst()

Room.GetNearby()

Room.GetNext()

Room.GetPresetUnits()

Room.UnitInRoom()


## Events


### EVENT_GAMEMSG


* Syntax:

RegisterEvent(EVENT_GAMEMSG, FunctionToCallOnEvent);
UnregisterEvent(EVENT_GAMEMSG, FunctionToCallOnEvent);
function FunctionToCallOnEvent(msg, type)
{ // your event code here }

* Description:

Controls registration for game event notifications.

* Parameter:

Where msg contains the chat message and type corresponds to message color
const NTC_COLOR_BASE_WHITE = 0;
const NTC_COLOR_BASE_RED = 1;
const NTC_COLOR_BASE_GREEN = 2;
const NTC_COLOR_BASE_BLUE = 3;
const NTC_COLOR_BASE_GOLD = 4;
const NTC_COLOR_BASE_GRAY = 5;
const NTC_COLOR_BASE_BLACK = 6;
const NTC_COLOR_BASE_GOLD2 = 7;
const NTC_COLOR_BASE_ORANGE = 8;
const NTC_COLOR_BASE_YELLOW = 9;

* Return Value(s):



* Notes:



* Example:

EVENT_KEYDOWN

EVENT_KEYUP

EVENT_SCRIPTMSG


# Installation instructions for Xorg X11

## Installation

Append this text to the xkb/symbols/us file of your X11 installation.

eg /usr/share/X11/xkb/symbols/us

```
// EngramMod 
partial alphanumeric_keys
xkb_symbols "EngramMod" {

	include "us"
	name[Group1]= "English (EngramMod)";

	key <TLDE> { [        grave,   asciitilde ] };
	key <AE01> { [            1,       exclam ] };
	key <AE02> { [            2,           at ] };
	key <AE03> { [            3,   numbersign ] };
	key <AE04> { [            4,       dollar ] };
	key <AE05> { [            5,      percent ] };
	key <AE06> { [            6,  asciicircum ] };
	key <AE07> { [            7,    ampersand ] };
	key <AE08> { [            8,     asterisk ] };
	key <AE09> { [            9,	     less ] };
	key <AE10> { [            0,   	  greater ] };
	key <AE11> { [  bracketleft,    braceleft ] };
	key <AE12> { [ bracketright,   braceright ] };

	key <AD01> { [            b,            B ] };
	key <AD02> { [            y,            Y ] };
	key <AD03> { [            o,            O ] };
	key <AD04> { [            u,            U ] };
	key <AD05> { [   apostrophe,    parenleft ] };
	key <AD06> { [	   quotedbl,   parenright ] };
	key <AD07> { [            l,            L ] };
	key <AD08> { [            d,            D ] };
	key <AD09> { [            w,            W ] };
	key <AD10> { [    	  v,        	V ] };
	key <AD11> { [ 		  z,   		Z ] };
	key <AD12> { [        equal,   underscore ] };
	key <BKSL> { [    backslash,          bar ] };

	key <AC01> { [            c,            C ] };
	key <AC02> { [            i,            I ] };
	key <AC03> { [            e,            E ] };
	key <AC04> { [            a,            A ] };
	key <AC05> { [        comma,     semicolon] };
	key <AC06> { [       period,        colon ] };
	key <AC07> { [            h,            H ] };
	key <AC08> { [            t,            T ] };
	key <AC09> { [            s,            S ] };
	key <AC10> { [            n,            N ] };
	key <AC11> { [		  q,   		Q ] };

	key <AB01> { [            g,            G ] };
	key <AB02> { [            x,            X ] };
	key <AB03> { [            j,            J ] };
	key <AB04> { [            k,            K ] };
	key <AB05> { [        minus,	    slash ] };
        key <AB06> { [         plus,     question ] };
        key <AB07> { [            r,            R ] };
        key <AB08> { [            m,            M ] };
        key <AB09> { [       	  f,      	F ] };
	key <AB10> { [        	  p,     	P ] };

	key <SPCE> { [        space,        space ] };

	// key <CAPS> { [    BackSpace,       Escape,       BackSpace,        BackSpace ] };

	// do NOT hardcode this switch; use the setxkbmap option instead!
	//include "level3(ralt_switch)"
};
```

## Switching between layouts
To clear any extra layouts then:
```
$ setxkbmap -layout us,us -variant ,EngramMod -option ""
```

To configure to interactively switch to a new layout with the right-alt (ie group key):
```
$ setxkbmap -layout us,us -variant ,EngramMod -option "grp:toggle"
```

Add this to the .bash_profile to keep the configuration for next time:
```
setxkbmap -layout us,us -variant ,EngramMod -option "grp:toggle"
```



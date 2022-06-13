##How do we use Icons and make them accessible?

## Wrong 
```<span class="icon-plus"></span>```

Example: No Example in Joomla core


Only sighted users see the icon, blind users see nothing. 
If the screenreader announces nothing, this could be ok for a decorative element. 
If the screenreader announces somthing, then it is an issue.

## Pure decoration
```<span class="icon-plus" aria-hidden="true"></span>```

Example: Quckicons on the backend dashboard

Ok 
IF the icon is decorative only 
AND if the meaning is obvious and world wide well-known. 

## Icon Legend - wrong? 
```<div><span class="icon-check" aria-hidden="true"></span><?php echo Text::_('COM_YOURTEXT_HERE'); ?></div>```

Example: Legend at the bottom of permission table in com_users

Not sure if this is correct (needs test)
Sighted users see an icon followed by a text explanation. 
BUT: Blind users get an explanation for something what they cannot see. (needs test)

## Visible Icon with invisible text
```<span class="icon-check" aria-hidden="true"></span><span class="visibility: hidden"><?php echo Text::_('COM_YOURTEXT_HERE'); ?></span>```

Example: Legend at the bottom of permission table in com_users
Correct: An icon which is visible for sighted users and a text which is announced by screenreaders but is not visible. 

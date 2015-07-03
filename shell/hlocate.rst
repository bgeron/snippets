
************************************
hlocate.fish: find in home directory
************************************

``locate`` will not work if your home directory is encrypted. I use this instead::

	function hlocate
		find ~  | grep -e $argv[1]  | sed "s|^$HOME|\~|"
	end

Now::

	bgeron@machine ~> hlocate test1234
	~/tmp/test1234.txt
	bgeron@machine ~>


This is a Fish_ script, but it should be easy to convert to bash syntax.


.. _Fish: http://fishshell.com/

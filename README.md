Forked/Inspired from https://github.com/vashisthg/StartPointSeekBar

SeekBAr with positive and negative values
Set the default first position when you want in the seebar
get the current value dynamically

Add: current value above the cursor. The value change dynamically with the cursor.

![ScreenShot](http://i.imgur.com/NymatH2.jpg)

Example code:
        
        //initialize your seekbar with you max and min value
        StartPointSeekBar<Integer> seekBar = new StartPointSeekBar<Integer>(-100, +100, this);
        //set the start cursor position (Value between 0 and 1)
        seekBar.setNormalizedValue(0.5);
        //do something on change listener event
        seekBar.setOnSeekBarChangeListener(new StartPointSeekBar.OnSeekBarChangeListener<Integer>()
        {
            @Override
            public void onOnSeekBarValueChange(StartPointSeekBar<?> bar, Integer value)
            {
                Log.d(LOGTAG, "seekbar value:" + value);
            }
        });

        // add RangeSeekBar to pre-defined layout
        ViewGroup layout = (ViewGroup) findViewById(R.id.seekbarwrapper);
        layout.addView(seekBar);




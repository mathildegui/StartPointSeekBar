Forked/Inspired from https://github.com/vashisthg/StartPointSeekBar

Add the current value above the cursor. The value change dynamically with the cursor.

![ScreenShot](http://i.imgur.com/NymatH2.jpg)

Example code:

        StartPointSeekBar<Integer> seekBar = new StartPointSeekBar<Integer>(-100, +100, this);
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




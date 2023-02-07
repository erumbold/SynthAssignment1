# Assignment 1

## Q1-6
Code for Questions 1-6 can be found in the `Assignment1` Jupyter notebook. For Q1-4, I defined a function `oscillator()` that takes in a wave shape, frequency, and sample rate and returns the corresponding signal. If `midi_note` is passed in, it converts the MIDI number to its frequency before returning the signal.

I defined another function `read_note_file()` that takes in the name of a .csv file. Each row has two values: MIDI number and duration in seconds. For each row, `oscillator()` is called with the row's values. The returned signal is concatenated to the rest to create the melody.

My `buffer()` function is similar to `oscillator()` except it takes in `start` and `end`, which are the sample indices for the start and end of the buffer. A 1-second signal is created by `oscillator()` and truncated according to `start` and `end`.

To create polyphony with these functions, I defined `poly_oscillator()` which calls `read_note_file()` for each of a list of filenames. These files each correspond to a different voice part in an arrangement of the theme for 2001: A Space Odyssey. Each of the returned signals are summed together.

## Q7
Code for Q7 can be found in the `Assignment1` Max patch. One side plays the given frequency value, the other takes in a MIDI number, converts it to its corresponding frequency, and plays the sinewave.

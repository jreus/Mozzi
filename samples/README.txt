To Prepare Samples for use in a Mozzi Sketch:

-- In Audacity
1. Mix sample file down to mono
2. 16384 - Make note of the sample rate, then change the project sample rate to Mozzi's Audio rate (in standard mode this is 16384)
3. Export as "Other uncompressed files/RAW (headerless), 8-bit PCM"

-- Python script
4. Run mozzify.py to convert the audio file into a header which can be included
    in Arduino programs.

> ./mozzify.py in_file.raw out_file.h table_name original_samplerate

Example:
> ./mozzify.py ../gsr_examples/Zone2SourceWorkshop/samples/a_R.raw /samples/a_R.h a_R 22050
> opened ../gsr_examples/Zone2SourceWorkshop/samples/a_R.raw
> wrote ../samples/a_R.h

5. As long as this header file is in your Arduino searchpath you should be good to use it in your sketches.
# JSON Format

I'd like to think that the JSON format is pretty straightforward, but that's pretty
difficult to argue.

First up: We need to define a few settings. Now I'm not gonna lie, I don't really
understand what any of these do.

```json
{
    "settings": "AE3366N",
    ...
}
```

Then we just need to set up a few local things; once again, I don't understand the
different values for `timezone`, all I know is that 6 is CST, work from there.

```json
{
    ...
    "timezone": 6,
    "dst": false,
    "city": "Madison",
    "airport": "MSN",
    ...
}
```

From there, the world is your oyster, add a few channels with a few listings,
they're pretty darn simple!

```json
{
  ...
  "channels": [
    {
      "number": 1,
      "id": "TST001",
      "callsign": "TST",
      "hilite": false,
      "althilite": false,
      "summary": false,
      "listings": [
        {
          "time": "00:00",
          "name": "Listing #1"
        },
        {
          "time": "01:00",
          "name": "Listing #2"
        },
        {
          "time": "02:00",
          "name": "Listing #3"
        }
      ]
    }
  ]
}
```

The only things that *could* use a little bit of exlpaining are the flags:
```json
{
  ...
      "hilite": false,
      "althilite": false,
      "summary": false,
  ...
}
```

`hilite` is the red background highlight, `althilite` is the blue background highlight, 
and `summary` marks it as a summary channel as well. Unfortunately, due to the way I 
programmed things, you **do** need to specify all of these options as false, even if
you aren't using them.
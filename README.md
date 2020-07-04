# qfield_theme_issue

Switching theme doesn't change the associated layer edit mask... but it does!

The layer "test" has two styles "type" and "name"; each style has a different customized
attributes mask, with the same name as the style. The project has two theme: the theme
"type" shows the layer "test" with the style "type"; the theme "name" show the layer "test"
with the sytle "name".

Observed behaviour in QField:

1) Open the application; open the project test; "type" theme is selected, points are red, label is "field1";

   -a) select one feature, open the edit mask; the mask of style "type" is open.

   -b) change theme, select theme "name"; points are green, label is "field2";

   -c) select one feature, open the edit mask; the mask of style "type" is open.

Close the application.

2) Open the application; open the project test; "type" theme is selected, points are red, label is "field1";

   -a) change theme, select theme "name"; points are green, label is "field2";

   -b) select one feature, open the edit mask; the mask of style "name" is open.

   -c) change theme, select theme "style"; points are red, label is "field1";

   -d) select one feature, open the edit mask; the mask of style "name" is open.

It seems, the feature is supported and it isn't. It's really confusing.

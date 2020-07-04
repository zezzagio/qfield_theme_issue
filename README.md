# qfield_theme_issue

Switching theme doesn't change the associated layer edit mask... but it does!

The layer "test" as two styles "type" and "name"; each style has a different customized
attributes mask, with the same name as the style. The project has two theme: the theme
"type" shows the layer "test" with the style "type"; the theme "name" show the layer "test"
with the sytle "name".

Observed behaviour in QField:

1) Open the application; open the project test; "type" theme is selected, points are red, label is "field1";
1.a) select one feature, open the edit mask; the mask of style "type" is open.
1.b) change theme, select them "name"; points are green, label is "field2";
1.c) select one feature, open the edit mask; the mask of style "type" is open.

Close the application.

2) Open the application; open the project test; "type" theme is selected, points are red, label is "field1";
2.a) change theme, select them "name"; points are green, label is "field2";
2.b) select one feature, open the edit mask; the mask of style "name" is open.
2.c) change theme, select them "style"; points are red, label is "field1";
2.d) select one feature, open the edit mask; the mask of style "name" is open.

It seems, the feature is supported and it isn't. It's really confusing.

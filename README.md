
# Rapport

- [x] Add a second activity:
`activity_second.xml` & `SecondActivity.java`
- [x] Add a button in the first activity that starts the second activity:
Added a button in `activity_main.xml`, bound it to a
private button variable in `MainActivity.java` and added an OnClickListener for event handling.
(next step shows code that starts the second activity)

```
button = findViewById(R.id.button);
button.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View view) {
        buttonClick();
    }
});
```

![](Screenshot_1.png)

- [x] Add data to the intent bundle using extras:
Complemented the code that starts the second activity with an
extra that stores a value, in this case it stores a String to the 'Variable' `NAME`.

```
private void buttonClick(){
    Intent intent = new Intent(this, SecondActivity.class);
    intent.putExtra("NAME", "Mattias B");
    startActivity(intent);
}
```

- [x] In the layout of the second activity add least one widget to show data from the intent:
Added two TextViews, first is set with a String resource and second receives its text value from the
intent.

```
final String text = getIntent().getExtras().getString("NAME");

textView = findViewById(R.id.textView2);
textView.setText(text);
```

![](Screenshot_2.png)

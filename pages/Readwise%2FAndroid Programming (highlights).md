title:: Readwise/Android Programming (highlights)
deck:: [[Other-Books::Android Programming]]
author:: [[Bill Phillips]]
full-title:: "Android Programming"
category:: #books

- ![](https://images-na.ssl-images-amazon.com/images/I/417fn1Op71L._SL200_.jpg)
- Highlights first synced by [[Readwise]] [[Monday, 06-02-2023]]
	- -
		- An activity is responsible for managing user interaction with a screen of information. #flashcard
		- ([Location 679](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=679))
	- -
	- -
		- Widgets are the building blocks you use to compose a user interface. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 765](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=765))
	- -
	- -
		- Buttons, text input controls, and checkboxes are all types of widgets. #flashcard
		- tags:: [[rosa]] [[pink]]
		- ([Location 767](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=767))
	- -
	- -
		- match_parent view will be as big as its parent wrap_content view will be as big as its contents require #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 850](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=850))
	- -
	- -
		- setContentView(int layoutResID) #flashcard
		- ([Location 957](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=957))
	- -
	- -
		- A resource is a piece of your application that is not code #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 961](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=961))
	- -
	- -
		- Resources for your project live in a subdirectory of the app/res directory. #flashcard
		- ([Location 964](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=964))
	- -
	- -
		- To generate a resource ID for a widget, you include an android:id attribute in the widget’s definition. #flashcard
		- ([Location 1010](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1010))
	- -
	- -
		- View findViewById(int id) #flashcard
		- ([Location 1056](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1056))
	- -
	- -
		- public static Toast makeText(Context context, int resId, int duration) #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 1141](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1141))
	- -
	- -
		- Toast.makeText(QuizActivity.this,                            R.string.correct_toast,                            Toast.LENGTH_SHORT).show(); #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 1174](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1174))
	- -
	- -
		- Model objects have no knowledge of the user interface; their sole purpose is holding and managing data. #flashcard
		- ([Location 1347](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1347))
	- -
	- -
		- View objects know how to draw themselves on the screen and how to respond to user input, like touches. #flashcard
		- ([Location 1351](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1351))
	- -
	- -
		- They contain “application logic.” Controllers #flashcard
		- ([Location 1356](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1356))
	- -
	- -
		- android:drawableRight="@drawable/arrow_right" #flashcard
		- ([Location 1692](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1692))
	- -
	- -
		- children of the FrameLayout need android:layout_gravity attributes. #flashcard
		- ([Location 1957](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=1957))
	- -
	- -
		- protected void onSaveInstanceState(Bundle outState) #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 2000](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2000))
	- -
	- -
		- A Bundle is a structure that maps string keys to values of certain limited types. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 2005](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2005))
	- -
	- -
		- Testing the implementation of onSaveInstanceState(…) is a good idea #flashcard
		- tags:: [[azul]] [[blue]]
		- ([Location 2052](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2052))
	- -
	- -
		- Log.d(TAG, "Current question index: " + mCurrentIndex); #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 2117](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2117))
	- -
	- -
		- An intent is an object that a component can use to communicate with the OS. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 2575](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2575))
	- -
	- -
		- Intent i = new Intent(QuizActivity.this, CheatActivity.class);                 startActivity(i); #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 2599](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2599))
	- -
	- -
		- i.putExtra(EXTRA_ANSWER_IS_TRUE, answerIsTrue); #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 2676](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2676))
	- -
	- -
		- startActivity(i); #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 2693](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2693))
	- -
	- -
		- mAnswerIsTrue = getIntent().getBooleanExtra(EXTRA_ANSWER_IS_TRUE, false); #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 2711](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2711))
	- -
	- -
		- startActivityForResult(i, REQUEST_CODE_CHEAT); #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 2762](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2762))
	- -
	- -
		- There are two methods you can call in the child activity to send data back to the parent:     public final void setResult(int resultCode)     public final void setResult(int resultCode, Intent data) #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 2765](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2765))
	- -
	- -
		- setResult(RESULT_OK, data); #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 2801](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2801))
	- -
	- -
		- The final step is to override onActivityResult(int, int, Intent) in QuizActivity to handle the result. #flashcard
		- ([Location 2815](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2815))
	- -
	- -
		- result.getBooleanExtra(EXTRA_ANSWER_SHOWN, false); #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 2824](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=2824))
	- -
	- -
		- The ViewAnimationUtils and its createCircularReveal method were both added to the Android SDK in API level 21, so this code would crash on a device running a lower version than that. #flashcard
		- ([Location 3060](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3060))
	- -
	- -
		- A fragment is incapable of getting a view on screen itself. Only when it is placed in an activity’s hierarchy will its view appear. #flashcard
		- tags:: [[pink]] [[rosa]]
		- ([Location 3228](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3228))
	- -
	- -
		- Notice that the container view is completely generic; #flashcard
		- tags:: [[orange]] [[naranja]]
		- ([Location 3429](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3429))
	- -
	- -
		- The steps to creating a UI fragment are the same as those you followed to create an activity: compose a user interface by defining widgets in a layout file create the class and set its view to be the layout that you defined wire up the widgets inflated from the layout in code #flashcard
		- ([Location 3450](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3450))
	- -
	- -
		- Its job is to present the details of a specific crime and update those details as the user changes them. #flashcard
		- ([Location 3519](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3519))
	- -
	- -
		- Fragment.onCreate(Bundle) #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 3525](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3525))
	- -
	- -
		- public View onCreateView(LayoutInflater inflater, ViewGroup container,             Bundle savedInstanceState) {         View v = inflater.inflate(R.layout.fragment_crime, container, false);         return v;     } #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 3559](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3559))
	- -
	- -
		- FragmentManager fm = getSupportFragmentManager();         Fragment fragment = fm.findFragmentById(R.id.fragment_container);         if (fragment == null) {             fragment = new CrimeFragment(); #flashcard
		- tags:: [[naranja]] [[orange]]
		- ([Location 3640](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3640))
	- -
	- -
		- A style is an XML resource that contains attributes that describe how a widget should look and behave. #flashcard
		- tags:: [[azul]] [[blue]]
		- ([Location 3904](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3904))
	- -
	- -
		- A theme is a collection of styles. #flashcard
		- tags:: [[azul]] [[blue]]
		- ([Location 3915](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3915))
	- -
	- -
		- Android provides density-independent dimension units that you can use to get the same size on different screen densities. #flashcard
		- tags:: [[blue]] [[azul]]
		- ([Location 3938](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3938))
	- -
	- -
		- dip.” You typically use this for margins, padding, or anything else for which you would otherwise specify size with a pixel value. #flashcard
		- ([Location 3947](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3947))
	- -
	- -
		- You will almost always use sp to set display text size. #flashcard
		- tags:: [[azul]] [[blue]]
		- ([Location 3953](https://readwise.io/to_kindle?action=open&asin=B0136ZXIMM&location=3953))
	- -
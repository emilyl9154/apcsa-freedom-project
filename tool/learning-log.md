# Tool Learning Log

Tool: **Android Studio (Java)**

Project: **A reminder app where you pin the reminder/task to your notifications, either immediately or timed**

---

10/27/23 - 10/28/2023:
* What I did:
    * Created a new project using the `Basic Views Activity` template
    * Using the template, made it so when you press a button the text changes from "Hello World!" to "Goodbye World!"

* Links used:
    * Android Studio [TextView](https://developer.android.com/reference/android/widget/TextView)
    * Specific attributes:
        * Customizing text: `textSize`, `textColor`, `textStyle`, `gravity` (alignment)
        * Customizing button: `backgroundTint`
        * Changing text value: `setText`
    * [Stack Overflow post](https://stackoverflow.com/questions/4768969/how-do-i-change-textview-value-inside-java-code) for changing the text

* Code
    * Changing text
        * ```java
          // activity_main.xml
          binding.button.setOnClickListener(new View.OnClickListener() {
              @Override
              public void onClick(View view) {
                final TextView theText = (TextView) getActivity().findViewById(R.id.text);
                theText.setText("Goodbye World!");
              }
          });
          ```
    * Customizing text & button
        * ```java
          // strings.xml
          <string name="text">
              Hello World!
          </string>
          ```
        * ```java
          // fragment_first.xml
          <TextView
              android:id="@+id/text"
              android:layout_width="311dp"
              android:layout_height="46dp"
              android:layout_marginTop="188dp"
              android:gravity="center"
              android:text="@string/text"
              android:textColor="#3592f0"
              android:textSize="30sp"
              android:textStyle="bold"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintHorizontal_bias="0.504"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toTopOf="parent" />

          <Button
              android:id="@+id/button"
              android:layout_width="241dp"
              android:layout_height="54dp"
              android:layout_marginTop="236dp"
              android:backgroundTint="#2470bd"
              android:text="Press me!"
              app:layout_constraintEnd_toEndOf="parent"
              app:layout_constraintHorizontal_bias="0.497"
              app:layout_constraintStart_toStartOf="parent"
              app:layout_constraintTop_toTopOf="parent" />
          ```

<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->

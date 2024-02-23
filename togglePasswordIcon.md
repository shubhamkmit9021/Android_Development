## how to implement show and hide password icon accordingly with the input field value also toggle

````
<LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="vertical"
                    android:paddingHorizontal="@dimen/_15dp"
                    android:layout_marginBottom="@dimen/_10dp">

                    <TextView
                        android:layout_width="wrap_content"
                        android:layout_height="wrap_content"
                        android:text="@string/login_pass"
                        style="@style/Headlines_16_Bold"
                        android:textColor="@color/labelBlack"
                        android:layout_marginBottom="@dimen/_2dp"
                        />

                    <LinearLayout
                        android:layout_width="match_parent"
                        android:layout_height="wrap_content"
                        android:layout_marginVertical="@dimen/_6dp"
                        android:layout_marginHorizontal="@dimen/_5dp"
                        android:gravity="center"
                        android:padding="@dimen/_4dp"
                        android:elevation="@dimen/_3dp"
                        android:backgroundTint="@color/white"
                        android:background="@drawable/editbox">

                        <LinearLayout
                            android:layout_width="@dimen/_0dp"
                            android:layout_height="wrap_content"
                            android:layout_weight="3.5">

                            <EditText
                                android:layout_width="match_parent"
                                android:layout_height="wrap_content"
                                android:id="@+id/editText_pass"
                                android:hint="@string/login_pass_hint"
                                android:maxLines="1"
                                android:singleLine="true"
                                android:inputType="textPassword"
                                android:backgroundTint="@color/white"
                                android:textColorHint="@color/placeholder"
                                style="@style/textInputStyle"
                                />

                        </LinearLayout>

                        <!-- Icon box  -->
                        <LinearLayout
                            android:layout_width="@dimen/_0dp"
                            android:layout_height="wrap_content"
                            android:layout_weight="0.5"
                            android:gravity="center"
                            android:layout_marginHorizontal="@dimen/_2dp"
                            >
                            <ImageView
                                android:layout_width="@dimen/_30dp"
                                android:layout_height="@dimen/_25dp"
                                android:scaleType="centerInside"
                                android:id="@+id/showHide_pass"
                                />

                        </LinearLayout>

                    </LinearLayout>

                </LinearLayout>
````
- In java file:-
- ***Inside onCreate called this function ..... togglePassword();***
````
private void togglePassword() {
        // for show hide password using eye icon functionalities
        showHide_pass.setImageResource(R.drawable.hidepass);
        showHide_pass.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if(editText_pass.getTransformationMethod().equals(HideReturnsTransformationMethod.getInstance())) {

                    // If password is visible then Hide it
                    editText_pass.setTransformationMethod(PasswordTransformationMethod.getInstance());

                    // Change Icon
                    showHide_pass.setImageResource(R.drawable.hidepass);

                } else {
                    editText_pass.setTransformationMethod(HideReturnsTransformationMethod.getInstance());
                    showHide_pass.setImageResource(R.drawable.show_pass);
                }
                // remove focus
                editText_pass.clearFocus();
            }
        });
    }
````

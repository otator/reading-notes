# Recycler View   

when large set of data that needs to be displayed whenever the user scroll up and down, it takes to mush of the memory size of the app, by creating the views, display them on the screen, and destroy them when they are nolonger on the screen, this also consume the battery power of the android device.

Recycler view can solve the previuos problem, its job is instead of create a view for each item, it creates fews views that can be displayed on the screen, and whenever the user scroll, the views that no longer on the screen, it reuse them to display new items instead of destroy them, this imrove the application performance, and consume less power and memory.

To implement the RecyclerView in your code you need to define a class that extends it, and override its three methods:
* `onCreateViewHolder()`: this method is to create a view holder
* `onBindViewHolder()`: this method is to fill the views with the data from the source
* `getItemCount()`: this method is to tell the recycler view how much the size of the data so it knows when there are no more view to display.



but first you need to create the view that you will hold the date and the layout that will have the views as its children.

The following [code](https://developer.android.com/guide/topics/ui/layout/recyclerview#tabpanel-java) is a custom class that extends the recycler view to create dynamic and reuseable views.

```java
  public class CustomAdapter extends RecyclerView.Adapter<CustomAdapter.ViewHolder> {

    private String[] localDataSet;

    /**
     * Provide a reference to the type of views that you are using
     * (custom ViewHolder).
     */
    public static class ViewHolder extends RecyclerView.ViewHolder {
        private final TextView textView;

        public ViewHolder(View view) {
            super(view);
            // Define click listener for the ViewHolder's View

            textView = (TextView) view.findViewById(R.id.textView);
        }

        public TextView getTextView() {
            return textView;
        }
    }

    /**
     * Initialize the dataset of the Adapter.
     *
     * @param dataSet String[] containing the data to populate views to be used
     * by RecyclerView.
     */
    public CustomAdapter(String[] dataSet) {
        localDataSet = dataSet;
    }

    // Create new views (invoked by the layout manager)
    @Override
    public ViewHolder onCreateViewHolder(ViewGroup viewGroup, int viewType) {
        // Create a new view, which defines the UI of the list item
        View view = LayoutInflater.from(viewGroup.getContext())
                .inflate(R.layout.text_row_item, viewGroup, false);

        return new ViewHolder(view);
    }

    // Replace the contents of a view (invoked by the layout manager)
    @Override
    public void onBindViewHolder(ViewHolder viewHolder, final int position) {

        // Get element from your dataset at this position and replace the
        // contents of the view with that element
        viewHolder.getTextView().setText(localDataSet[position]);
    }

    // Return the size of your dataset (invoked by the layout manager)
    @Override
    public int getItemCount() {
        return localDataSet.length;
    }
}

```

```xml
  <FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="@dimen/list_item_height"
    android:layout_marginLeft="@dimen/margin_medium"
    android:layout_marginRight="@dimen/margin_medium"
    android:gravity="center_vertical">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/element_text"/>
</FrameLayout>

```


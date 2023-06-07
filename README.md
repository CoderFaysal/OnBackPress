# OnBackPress

```
    @Override
    public void onBackPressed() {
        final AlertDialog.Builder builder = new AlertDialog.Builder(this);
        builder.create();
        builder.setTitle("App Name");
        builder.setMessage("Do you want to exit the app?");
        builder.setCancelable(false);
        builder.setPositiveButton(
                "Yes", new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        finish();
                    }
                }
        );
        builder.setNegativeButton(
                "No, Thanks",
                new DialogInterface.OnClickListener() {
                    @Override
                    public void onClick(DialogInterface dialog, int which) {
                        dialog.cancel();
                    }
                }
        );
        builder.show();
    }
```

# todolist
a to-do list that generates flowers each time a task is completed

pen and paper to-do lists don't give you a hit of dopamine; they just give you hand cramps. i decided i wanted a to-do list that actually celebrated my wins.

every time you tick off a task in this Excel sheet, a new flower is "generated."

it's just a single formula that counts your checkboxes and pulls an image from a "seed bank" (your list of links).


the formula

if you want to build this yourself or customize the garden, here is the logic i used:

=IMAGE(
    INDEX(
    
        {
        
        "Image 1 Link",
        
        "Image 2 Link",
        
        "Image 3 Link",
        
        "Image 4 Link",
        
        "Image 5 Link",
        
        "Image 6 Link",
        
        "Image 7 Link",

        "Image 8 Link"
        
        },
        
        MIN(8, COUNTIF($A$1:$A$8, TRUE) + 1)
        
    )
    
)

you can also upload your images to Google Drive (or any image hosting site).

ensure the links are set to "Anyone with the link can view."

replace "Image 1 Link", "Image 2 Link", etc., in the formula above with your direct image links.

update the range $A$1:$A$8 to match wherever your checkboxes live

when you save your Excel file for the repo, make sure you save it as an .xlsx (Excel Workbook) rather than an old .xls, as the =IMAGE() function is a newer feature that works best in modern Excel versions and Excel for the Web!

[watch the growing flower demo](growingflowerdemo.mov)

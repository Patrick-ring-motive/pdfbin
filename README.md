# pdfbin
This is a project to store pdf files for later posting on social media.

## Why
Currently most social media sites to not provide descriptions or thumbnails for links to pdf files. This project was built specifically for that purpose. The pdfs are preceded by a simple html containing OGP(open graph protocol) so that the social media post links contain preview images and titles. This is a simple and straight forward solution that is necessary until either PDF is made compatable with OGP or OGP is made to read PDF tags.

## Example
https://www.reddit.com/r/mealybugs

This was created so initially for creating posts on reddit r/mealybugs so you can view the prime examples in the pdfbin links on https://www.reddit.com/r/mealybugs

This repo is hosted at https://pdfbin.vercel.app/ and an example link is https://pdfbin.vercel.app/mealybugs/ncipmc.org/Papaya-Mealybug/Papaya-Mealybug.html

## Structure
The form of the structure contains 3 files.

*PDF - this is the original .pdf acrobat file that you want to post on social media. You could use any sort of file here but pdf is one of the most used files that is least compatable with OGP and older webscraping methods.

*image - this is an image that you want to use as the preview icon on your social media post. OGP is finicky about using different image types so I have elected to use .jpeg format since it is the most widely accepted format there.

*html - this is the html file that contains all of the meta tags related to OGP that are picked up by web scrapers and socal media sites. I also include a redirect meta tag and a javascript redirect that will ensure that the user is only routed through the html page on the first access. Subsequent accesses will go directly to the pdf.



## Ref
Just putting this link here for my reference

https://ogp.me/

https://github.com/ngduc/vercel-express

https://vercel.com/docs/project-configuration

## TODO
Intending to create a single portable file instead of 3 separate files. This is possible but proved to be more effort than necessary for little gain. Also would have had to probably compress the thumbnail image to less than 2 mb and use blob links for pdfs which are not great for sharing. Might come back to this later. Learned a lot about blob links, data encoding, and image compression from trying so I will keep some examples around in the test folder.
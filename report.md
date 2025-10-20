for the first 2 objectives:
1. Analyze and finding correct window size in identifying a segment.
for this, i think 3x3 matrix is enough to identify a segment because the size of a points but not sure for the line because it have 4-pixel wide.


2. Report all fitting of appropriate window pattern for identifying a segment. 
i modify a few lines from the source code given:
for(int m=-1;m<=1;m++){
                for(int n=-1;n<=1;n++){
                    QRgb rgbValue = image.pixel(i+m, j+n);
                    if (local_window[m+1][n+1] = (rgbValue != 0xffffffff)) {               <--------
                        cout << "non empty window = (" << i << "," << j << ")" << endl;    <--------
                    }
                }
            }
these lines will check with if statement to check if the local window detect a color other than white
if true, print the window coordinate (x,y)

https://www.perplexity.ai/search/how-to-find-scan-non-empty-win-nSCAgfR0SNWakbyGJ3mTdA#1
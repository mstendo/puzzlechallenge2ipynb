# puzzlechallenge2ipynb
this program involves a scrambled 9 X 9 image puzzle made of 81 square pieces. Each piece may be rotated. the goal is to reconstruct the original image by comparing the edges of each piece and finding the best-fitting neighbors. The code rotates each piece, extracts its edges, compares them using pixel similarity, and assembles the puzzle row by row. The final image is stitched together and saved
pseudocode
load scramble puzzle data from file
extract image dta from each puzzle piece
for each piece:
a) generate all 4 rotations
b)for every other piece j( j not equal to i):
i) for each j rotation:
 - compare i's right edge with j's left edge
 - compare i's bottom edge with j's lefy edge
 - if similarity is better, update best match
store best right and bottom matches for each piece
create an empty 9 x 9 grid
place the first piece (index 0) in the top left corner
for each row:
 - fill the row by following best right matches
 - move to the next row using the best bottom match of the last piece
stitch all rows and coloumns into one image
save the final image as "solved_puzzle.png"


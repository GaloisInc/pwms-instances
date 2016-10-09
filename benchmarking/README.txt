USE GNUPLOT to regenerate the images, replace aaa.png with the name of the image you want to generate, and 300900b.csv by the csv you want to use.


set palette defined (0 "red", 1 "white" ,2 "blue")
set datafile separator ","
set term png size 1000,1000
set output "aaa.png"
set xlabel "Handlers"
set ylabel "Resources"
set zlabel "Locks"
set grid xtics
set grid ytics

splot "300900b.csv" using 1:2:3:($14-$28+1) with points pt 5 ps 3 palette
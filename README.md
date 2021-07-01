# introduction #
gaussian process bayesian optimization visualization.ipynb

## code descrition ##

* use less samples to find the maximum value in test function(Branin Rosenbrock)
* generate 20 points in x y dimension
* in order to plot the 3D function, use meshgrid to get the points
* means 20*20 = 400 samples are necessary to plot the function
* all data = 400 samples = design_domain + train_set
* use train_set -> GP to get a surrogate model  
* use design_design -> BO to find to good point and add it to train_set 
* (train_set + good point) + (design_domain - good point) = all_data
* if in some epochs, the good point change little, stop iteration


##  you can choose Branin or Rosenbrock by select the cell.

![avatar](https://github.com/WholeG/GPBO/raw/main/pictures/rosenbrock_max_0.jpg)

- the green points are train set
- the gray plane is the true function branin, use 400 points by meshgrid()
- the red plane is the prediction of GP on design_domain(all data train set)
- the red vertical line and the blue star point tell us the next point that should be added


![avatar](https://github.com/WholeG/GPBO/raw/main/pictures/rosenbrock_max_11.jpg)

- after some iterations , the predction is close to the true function 

![avatar](https://github.com/WholeG/GPBO/raw/main/pictures/max_round.jpg)
- the maximum of acquistion function, actually, iteration8 is the best.
## About author

```javascript
var ihubo = {
  nickName  : "Duke",
  site : "https://github.com/WholeG/GPBO"
}
```

# st-petersburg-paradox
The St. Petersburg paradox is a famous problem in probability theory and economics. It shows that the expected value (mathematical average payoff) of a simple gambling game is infinite, yet in reality, people are only willing to pay a modest amount to play.

It was first formulated by Daniel Bernoulli in 1738 (published in a journal based in St. Petersburg, hence the name).

### The game works like this:
A fair coin is tossed repeatedly until it comes up heads.
If heads comes up on the first toss, you win 2 euros.
If it first comes up on the second toss, you win 4 euros.
If it first comes up on the third toss, you win 8 euros.

And so on, the payout doubles for each additional toss required.

The expected payout of this experiment is
E(X) = inf

### Why did i make this short code?
I figured even though the expected return on the investment is infinite, there has to be a way to price it.

#### Let's say you're the casino owner, what price should you take

The reason as to why I track the highest gain is because I suspected that the average return is highly dependent on a single lucky streak. 
This seems to be the case, which makes pricing even harder. 

Further, as you're so at risk from a single lucky streak, the "average average" increases slightly the more iterations you do. 
Therefore you're going to have to make an estimation on how many throws will be thrown in total.
Let's say the dealer throws 3 coins a minute, 8 hours a day for 10 years straight
3 * 60 * 8 * 365 * 10 = 5256000

#### You could make a for loop and store every average value in an array and use numpy to find the mean and the variance, and make an interval of confidence (intervalle de confiance à 99%)
However given the fact that you would then have to simulate millions, of not near a billion throws, with my code that runs super slowly.

I've done it manually and just eyeballed it, because I'm not a statistician but an electrical engineer who just so happened to have a stats class last semester.
I consistenly get an average of around 21-23 running my simulations one by one, with an average of 20-22 if we disregard the luckiest streak.

However, sometimes, and not not that even that infrequently it shoots up to around 40-60.

### Conclusion
I would personally price the game around 25 to 28 euros. You'd most likley be fine and rake in some money offering this game at that price. The individual player would lose a lot of money playing against you, as the "average average" for playing very few games is around 8 euros. 

The expected value of one hand is still of course infinite, and you'd be reckless to offer this game to anyone. But at my price the chance of someone making a profit off you on a single had is around 3%. I'd love to have more computing power to actually be able to do some more simulations on this. 

Next year i'll be learning assembly, perhaps like that I can make the time to make a more smooth simultiion.

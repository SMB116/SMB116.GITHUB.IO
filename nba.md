# Data Don't Lie: An In-Depth Analysis of Toronto Raptors' Performance 2021-2022 Season

Being a Canadian basketball fan can be tough, as we only have one home team to cheer for out of the 30 NBA teams. 

Although we used to have two, the Vancouver Grizzlies are no longer with us – I won't delve into the details of how they were lost. 

As a Canadian, I can't say I'm overly patriotic when it comes to basketball; I've always been a Lakers fan. However, when the Toronto Raptors won the 2019 NBA championship, I couldn't help but root for them. It was a moment of pride for all Canadians. 

If you weren't feeling like Drake during that whole playoff run, I don't know what you were doing.

<div style="text-align: center;">
<img src="images/Drake Gif.gif?raw=true"/>
</div>

We've had chances to win in the past, with legends like Vince Carter and Tracy McGrady, but we always fell short. Playing in Canada isn't the most attractive option for players, considering the cold weather and Canadian taxes, eh? However, when we acquired Kawhi Leonard and won the championship, it was something special for the entire country.

Unfortunately, every good thing must come to an end, and the 2021-2022 season was no different for the Toronto Raptors. Once again, we were eliminated from the first round of the playoffs, marking the 7th time this has happened. All our potential and hopes were shattered in the first round, losing to the 76ers 2-4.

As a data analyst working for the team at the end of the season, I delved into the statistics to identify areas for improvement. It's well-known that "ball don't lie," so analyzing the data is the best way to understand where the team can make progress.

Utilizing data from the provided dataset from the website Basketball Reference (You can access the dataset [here](https://www.basketball-reference.com/leagues/NBA_2022_totals.html)), I am able to obtain accurate basketball statistics. However, due to the inclusion of players who were traded multiple times, data cleaning is required to ensure the accuracy and consistency of the analysis.

## Toronto Raptors' Strategic Initiatives for the 2021-2022 Offseason
**Areas of Focus:**
The Toronto Raptors strategically prioritized frontcourt improvement, three-point shooting, and perimeter defense during the 2021-2022 offseason to position themselves for success in the upcoming season. Addressing the needs at center and power forward, the team aimed to enhance their interior defense, rebounding, and overall frontcourt presence. Additionally, their focus on enhancing three-point shooting and perimeter defense underscores their commitment to building a well-rounded and competitive team.

**Key Questions:**
- **Recognizing Playmaking Contributors:** Who Are the Key Playmakers on the Team?
- **Identifying Shooting Improvement:** Which Position Needs More Improvement in 3-Point Shooting?
- **Evaluating Rebounding Efficiency:** How Does Our Rebounding Performance Compare to Other Teams?
- **Strengthening Shot Blocking:** Which Position Requires Improvement for Blocks in Interior Defense?

## Key Insights:
- Small Forward and Power Forward positions need improvement in 3-point shooting. Targeting their shooting improvement can elevate the team's offensive capabilities.
- The top playmakers on the Toronto Raptors are Fred VanVleet, Pascal Siakam, Scottie Barnes, and Gary Trent Jr. They have shown promising potential in creating scoring opportunities for the team.
- The Toronto Raptors rank second in the league for offensive rebounds, providing them with valuable second chance opportunities.
- However, their defensive rebounding ranks last in the league, indicating an urgent need to improve their rebounding efficiency on the defensive end.
- For interior defense, the Centers need improvement for blocks as they rank third in the team's blocks statistics. Strengthening their shot-blocking capabilities can bolster the team's defensive performance.

# Data Don't Lie: An In-Depth Analysis of Toronto Raptors' Performance

## The Playmakers: Recognizing Key Contributors in the Toronto Raptors Squad

We'll begin by delving into the playmakers of this season.

Recognizing the key playmakers holds immense importance in fine-tuning the team's offensive strategies. Playmakers assume a vital role in creating scoring chances for their fellow teammates, orchestrating ball movement, and establishing a harmonious offensive rhythm.

Therefore, I aimed to construct a bubble plot to identify our foremost scorers and assist leaders, with the bubble size reflecting the assist-to-turnover ratio. This approach enables us to assess how our players stack up against their counterparts across the league.

<img src="images/Bubbleplot.jpg?raw=true"/>

Indeed, no particular players stand out within the team.

Nevertheless, there are four individuals who surpass the general player cluster: Fred VanVleet (point guard), Pascal Siakam (power forward), Scottie Barnes (power forward), and Gary Trent Jr (shooting guard). 

This accentuates the proficiency of our power forward position, as these players exhibit promising potential.

Furthermore, these players demonstrate low assist-to-turnover ratios, indicative of their adeptness in ball control and making sound decisions on the court.

## Beyond the Arc: Analyzing Toronto Raptors' 3-Point Shooting Performance

Now, let's redirect our attention to the 3-point shooters.

Through the identification of the frontcourt position exhibiting lower three-point shooting percentages, we can strategically channel our endeavors towards refining player skills and considering potential roster adjustments to bolster outside scoring. By enhancing shooting proficiency from this position, we can elevate the team's offensive prowess and amplify overall scoring efficiency.

To attain a comprehensive grasp, we will generate a heatmap that juxtaposes the league's 3-point percentage.

This visualization will provide us with insights into the Toronto Raptors' performance across different positions in comparison to the league average, allowing us to pinpoint specific areas that necessitate improvement.

<img src="images/Heatmap.jpg?raw=true"/>

The heatmap clearly shows that the Toronto Raptors struggle with three-point shooting in the Center, Power Forward, and Small Forward positions, performing below the league average.

To improve offensive efficiency and scoring, investing in player development and potential roster changes for better outside shooting is crucial. This will help the Raptors compete at a higher level in the league.

## Rebounding Rundown: Assessing Toronto Raptors' Offensive and Defensive Board Dominance

Time to evaluate the team's rebounding performance.

Identifying the frontcourt position that needs improvement in rebounds is crucial for enhancing both defensive and offensive rebounding efficiency. Improved rebounding not only prevents opponents from scoring in the paint but also contributes to gaining possession through rebounds.

By strengthening our rebounding capabilities, the team can increase their chances of securing both defensive and offensive rebounds, ultimately enhancing overall defensive stability and rebounding efficiency.

To gain a comprehensive perspective, I utilized a stacked bar chart that breaks down the amount of defensive and offensive rebounds, highlighting the leading rebounders on our team.

This visualization allows us to assess how Toronto compares in both defensive and offensive rebounding aspects and identify key contributors to our rebounding efforts.

Let's begin with the positive aspect of offensive rebounds.

<img src="images/OffenseRebounds.jpg?raw=true"/>

Scottie Barnes and Chris Boucher take the lead for the Toronto Raptors in this category.

As a collective unit, the Raptors secure the second spot in the league for offensive rebounds, granting them valuable second chances to capitalize on scoring opportunities. Sustaining this level of performance is essential to consistently maximize offensive efficiency and capitalize on scoring chances.

Now, let's shift our focus to defensive rebounds:

<img src="images/DefenseRebounds.jpg?raw=true"/>

With defensive rebounds, a different and concerning situation arises. Despite Pascal Siakam's leadership in this area, the Toronto Raptors exhibit the league's lowest defensive rebounding statistics. 

This highlights the need for improvement in securing defensive stops and preventing opponents from seizing second-chance scoring opportunities due to missed rebounds. Addressing this issue is of utmost importance to enhance our defensive performance and curtail our opponents' scoring opportunities.

## Blocking Breakdown: Analyzing Toronto Raptors' Interior Defense and Shot-Blocking Dominance

Lastly, our focus shifts to shot-blocking. Recognizing the frontcourt position that demands enhancement in shot-blocking is essential for fortifying our interior defense. Enhanced shot-blocking serves as an effective deterrent against opponents scoring in the paint, thereby contributing to the overall stability of our defense.

For a visual representation, I employed treemaps, segmenting blocks by position. By assigning positions to the "Color" tab and adjusting size, we gain insights into the shot-blocking performance of each position.

This visualization enables us to pinpoint the specific positions that necessitate improved shot-blocking, ultimately reinforcing our defensive capabilities and discouraging opponents from scoring within the paint.

<img src="images/Blocks.jpg?raw=true"/>

At present, the team's block contributions are predominantly coming from the small forwards and power forwards, a significant observation. 

Nevertheless, the fact that our centers are ranked third in blocks gives rise to concerns, highlighting a potential vulnerability in safeguarding the paint.

**Recap of Key Insights:**
- Small Forward and Power Forward positions show potential for improvement in 3-point shooting. Enhancing their shooting can enhance the team's offensive capabilities.
- The Toronto Raptors' top playmakers include Fred VanVleet, Pascal Siakam, Scottie Barnes, and Gary Trent Jr. Their ability to create scoring opportunities is promising for the team's success.
- Toronto Raptors hold the second position in the league for offensive rebounds, creating valuable second-chance opportunities.
- However, their defensive rebounding ranks at the bottom of the league, highlighting the urgency to enhance rebounding efficiency on defense.
- The Centers' shot-blocking performance ranks third on the team. Strengthening their shot-blocking abilities can contribute to an improved defensive performance.

Don't forget to [check out my interactive Tableau story](https://public.tableau.com/app/profile/shekela/viz/NBA_16912797295950/Story1?publish=yes)!

<a href="javascript:history.back()" style="display: inline-block; padding: 10px 20px; background-color: #007bff; color: #fff; text-decoration: none; border-radius: 4px;">Go Back</a>


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

Let's begin by understanding who the playmakers were this season. 

Identifying the primary playmakers is crucial for optimizing the team's offensive strategies. Playmakers play a significant role in setting up scoring opportunities for their teammates, facilitating ball movement, and creating a cohesive offensive flow.

I also wanted to see a bubble plot to determine our top scorer and assist leaders, with the size of the bubble representing blocks. This will help us gauge how our players measure up to the rest of the league.

<img src="images/Bubbleplot.jpg?raw=true"/>

As observed, there are no standout players on the team. However, we have four players who excel above the cluster of players: Fred VanVleet (point guard), Pascal Siakam (power forward), Scottie Barnes (power forward), and Gary Trent Jr (shooting guard). This highlights our strength in the power forward position, as these players show promising potential. Additionally, Chris Boucher (small forward) stands out as their top blocker.

## Beyond the Arc: Analyzing Toronto Raptors' 3-Point Shooting Performance

Let's shift our focus to the 3-point shooters. 

By identifying the frontcourt position with lower three-point shooting percentages, we can direct our efforts towards player development and potential roster changes to enhance outside scoring. Improving shooting from this position will elevate the team's offensive capabilities and increase overall scoring efficiency.

To gain a comprehensive understanding, we'll create a heatmap comparing the league's 3-point percentage. This will enable us to assess how the Raptors perform in each position relative to the league average and pinpoint areas that require improvement.

<img src="images/Heatmap.jpg?raw=true"/>

As evident from the heat map, the Toronto Raptors' three-point shooting in the Center, Power Forward, and Small Forward positions falls below the league average for each specific position. Addressing this concern is vital for improving the team's offensive efficiency and scoring capabilities. By investing in player development and considering potential roster changes to strengthen outside shooting, the Raptors can elevate their offensive performance and compete at a higher level in the league.

## Rebounding Rundown: Assessing Toronto Raptors' Offensive and Defensive Board Dominance

Next, let's delve into the team's rebounding performance. 

Identifying the frontcourt position that requires improvement in shot-blocking is vital for enhancing both interior defense and rebounding efficiency. Improved shot-blocking not only deters opponents from scoring in the paint but also contributes to gaining possession through defensive rebounds.

To gain a comprehensive perspective, I utilized a stacked bar chart, which breaks down the amount of defensive and offensive rebounds, and highlights the leading rebounders on our team. This visualization allows us to assess how Toronto compares in both aspects and identify key contributors to our rebounding efforts.

<img src="images/OffenseRebounds.jpg?raw=true"/>

Starting with offensive rebounds, Scottie Barnes and Chris Boucher lead the way for the Toronto Raptors. As a team, the Raptors rank second in the league for offensive rebounds, giving them valuable second chance opportunities to capitalize on scoring chances. It is crucial to maintain this level of performance to continue maximizing scoring opportunities and offensive efficiency.

<img src="images/DefenseRebounds.jpg?raw=true"/>

When it comes to defensive rebounds, the situation is quite different and concerning. While Pascal Siakam leads the team in defensive rebounds, the Toronto Raptors have the lowest defensive rebounding statistics in the league. This indicates that there is room for improvement in securing defensive stops and preventing opponents from capitalizing on second-chance scoring opportunities due to missed rebounds. Addressing this issue is crucial to strengthen our defensive performance and limit our opponents' scoring opportunities.

## Blocking Breakdown: Analyzing Toronto Raptors' Interior Defense and Shot-Blocking Dominance

Lastly, let's turn our attention to shot-blocking. 

Identifying the frontcourt position that requires improvement in shot-blocking is vital for enhancing interior defense. Improved shot-blocking effectively discourages opponents from scoring in the paint, contributing to overall defensive stability.

To visualize this, I used treemaps, breaking up the blocks by position. By dragging positions to the "Color" tab and utilizing size, we can gain insights into the shot-blocking performance of each position. This visualization allows us to identify the specific positions that need improvement in shot-blocking to bolster our defensive capabilities and deter opponents from scoring inside the paint.

<img src="images/Blocks.jpg?raw=true"/>

Currently, the team's blocks are being primarily contributed by the small forwards and power forwards, which is noteworthy. However, the fact that our centers rank third in blocks raises some concerns, as it indicates a potential vulnerability in protecting the paint.

**Recap of Key Insights:**
- Small Forward and Power Forward positions show potential for improvement in 3-point shooting. Enhancing their shooting can enhance the team's offensive capabilities.
- The Toronto Raptors' top playmakers include Fred VanVleet, Pascal Siakam, Scottie Barnes, and Gary Trent Jr. Their ability to create scoring opportunities is promising for the team's success.
- Toronto Raptors hold the second position in the league for offensive rebounds, creating valuable second-chance opportunities.
- However, their defensive rebounding ranks at the bottom of the league, highlighting the urgency to enhance rebounding efficiency on defense.
- The Centers' shot-blocking performance ranks third on the team. Strengthening their shot-blocking abilities can contribute to an improved defensive performance.

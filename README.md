# Data for “Twitter is Throttling Patreon Links, Creators Say It Undermines Their Livelihood”

Here is the data for our story "[Twitter is Throttling Patreon Links, Creators Say It Undermines Their Livelihood](https://themarkup.org/news/2023/10/16/twitter-is-throttling-patreon-links-creators-say-it-undermines-their-livelihood)"
Markup readers helped uncover the link delays, which also affect WhatsApp and Messenger. Read the [full story](https://themarkup.org/news/2023/10/16/twitter-is-throttling-patreon-links-creators-say-it-undermines-their-livelihood).


# Methodology
In September, [The Markup reported](https://themarkup.org/investigations/2023/09/15/twitter-is-still-throttling-competitors-links-check-for-yourself) that Twitter, now officially named X, was slowing down links to Bluesky, Facebook, Instagram, and Substack, by an average of 2.5 seconds, which can feel extremely slow for users. We simultaneously launched a [tool](https://themarkup.org/investigations/2023/09/15/twitter-is-still-throttling-competitors-links-check-for-yourself) that lets readers test any link posted on X (links the platform automatically shortens using the t.co domain), and that measured the time it took for X to redirect the link to its original destination. The Markup also built a bot that would let us know if any links readers were testing appeared to be throttled.

Shortly after publication, readers began [using our tool](https://twitter.com/dancow/status/1705288111326990701), and we received alerts that Patreon, WhatsApp, and Messenger links appeared to be throttled. To confirm these findings, we created new links and measured from Oct. 11, 2023 at 8pm UTC through Oct. 16, 2023 at 12pm UTC the performance of redirects to the [25 top-earning Patreon campaigns](https://graphtreon.com/top-patreon-earners), as measured by tracking site Graphtreon on September 30.

During that time, we also tested 25 randomly selected, recently tweeted links to both WhatsApp and Messenger. With the exception of six Messenger links that do not seem to be throttled, we consistently found the same approximately 2.5-second slowdown. We do not know why most, but not all, links to Messenger’s m.me domain are throttled.

Questions? Write to us: [keegan@themarkup.org](mailto:keegan@themarkup.org) 

# Data

**[test_results_redacted.csv](https://github.com/the-markup/investigation-twitter-patreon/blob/main/test_results_redacted.csv)** - 5 KB KB. 76 rows. First row is the header (CSV).

This file contains a summary of our test results, grouped by the unique 75 t.co links in our test pool.

We have redacted the t.co and exapnded URLs for Whatsapp links, as they contained phone numbers. 

<table border="0" class="dataframe">
  <thead>
    <tr style="text-align: left;">
      <th>Column</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>tco_link</strong></td>
      <td>The shortened t.co link from X.</td>
    </tr>
    <tr>
      <td><strong>expanded_url</strong></td>
      <td>The expanded, or full URL of the link.</td>
    </tr>
      <tr>
      <td><strong>average_time</strong></td>
      <td>The average time for the link to be resolved in milliseconds. Each test measured the amount of time in milliseconds it took for X to expand a shortened URL for a given domain.</td>
    </tr>
     <tr>
      <td><strong>number_of_tests</strong></td>
      <td>The number of times we tested this link.</td>
    </tr>
  </tbody>
</table>

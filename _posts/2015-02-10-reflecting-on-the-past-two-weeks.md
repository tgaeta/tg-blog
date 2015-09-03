---
layout:     post
title:      Reflecting on the Past Two Weeks
date:       2015-02-10 07:00:00
summary:    Already?! 2 Weeks??!
categories: the-iron-yard ruby-on-rails ruby
---

It has already been two weeks since class started. In the span of 14 days, I have crammed in more knowledge about object oriented programming (OOP) than I thought possible.

A brief time-line of what I have learned so far:
<iframe src="http://cdn.knightlab.com/libs/timeline/latest/embed/index.html?source=0AjbUkbWZW6i_dHJ3VURneFRDTjdyZzZqMVJPZ25UX0E&amp;font=DroidSerif-DroidSans&amp;maptype=toner&amp;lang=en&amp;height=650" width="100%" height="650" frameborder="1"></iframe>

This is without a doubt the toughest course I've ever been through, but I absolutely love it. It can be frustrating at times... extremely frustrating. But I'm not giving up. My nights have gone from a 10 o'clock shut-eye to leaving the school house around 10:30 PM. I'm up most nights till 1:30 AM finishing homework while trying to cement the concepts I've been taught. I'm exhausted but I want more.

## Pig Latin
Here is a sample project of the Pig Latin script I wrote if you want to play around with it:
{% highlight ruby lineanchors %}
class String  
  VOWELS =  %w(a e i o u)
  def pigatize
    piglatin = ''
    split(' ').each do |word|
      if starts_with_vowel(word[0])
        piglatin += word + 'way'
      else
        piglatin += word[1..-1] + word[0] + 'ay' + ' '
      end
    end
    piglatin.chomp
  end
  def starts_with_vowel(first_letter)
    VOWELS.include?(first_letter)
  end
end
{% endhighlight %}
Pretty basic, huh? Yeah, well that took me a good weekend to figure out.

## Awesome Sidenote
So I entered into the St. Petersburg Chamber's Scholarship contest for the The Iron Yard's students. The essay topic was 'What Would You Build' and the scholarship prize was $3000. I WON! I was very excited to read about The Chamber's decision.

The Essay:

> In the 28 years that I have been a resident of St. Petersburg, I have witnessed the transformation from economic decline to a revitalization that has placed St. Pete as a top destination in the world by the New York Times. Without a doubt, the place that I love and call home has seen a boom in the arts, urban development, and the emergence of many awesome eateries and breweries. This welcomed transformation has encouraged the tech industry to setup shop at the epicenter of St. Pete’s revitalization, and The Iron Yard is here to foster St. Pete’s tech future.
>
> Now, what will I build? I will build a job board for St. Pete. The rapidly changing job market in St. Pete needs a job board that local businesses and job seekers can rely on. A quick look on Google will reveal that “jobs in St. Pete” is muddied with Monster, LinkedIn, Indeed, Glassdoor, and many other job behemoths. This job board will foster a ‘Keep St. Pete Local’ mentality by offering local businesses to advertise jobs at a very affordable price while allowing job seekers an easy experience to apply. This job board will also engage with local universities and SPC to help reach recent graduates.
>
> The features of this job board will include easy resume upload, mobile and tablet ready, job notifications, filterable by types of jobs (freelance, part-time, full-time, contract), and social media sharing for mass dissemination.

So needless to say, I am building a job board for St. Pete as my graduation demo app! Thank you to [St. Petersburg Chamber](http://www.stpete.com/) and [The St. Pete Greenhouse](http://stpetegreenhouse.org/) for choosing my essay. Now... back to work :)

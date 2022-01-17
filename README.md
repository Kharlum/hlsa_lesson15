# Task  
Peak load solution for European football website https://goal.com  

# Parts of the site that are expected to peak load  
- live scores  
- web push  
- main page (endless scroll)  

# Static web contents  
- Transfers  
- Breaking News  
- Premier League  
- UEFA Champions League  
- European Football  
- Women's Football  
- Contact Us  
- Terms of Service  
- Privacy Policy  
- Privacy Settings  
- Careers  

# Solutions to peak load problems  

1) short polling request:  
Unification of content (don't personalization content) and systematization of incoming parameters for use as "stacked" cache keys. Maximization of content caching and use preconditioning of cache (when changes in the content administrator - avoid completely purge the cache).  
2) static content:  
Caching and use geo-cdn. Use localStorage browser.  
3) web-push:
Use preconditioning of cache.
4) endless scroll:
Systematization of incoming parameters for use as "stacked" cache keys. Maximization of content caching and use preconditioning of cache (when changes in the content administrator - avoid completely purge the cache).  
5) image/video:  
Use geo-cdn.  
For video - don't use autoplay.  
For image - create image preview.  
6) championships:  
Championships of local importance - scale the system using the nearest data center.  
World Championship - follow the schedule of matches and scale the system into expected "hot" matches.  
7) DDoS attacks and/or bots activities:  
Use ready-made solutions (cloudflare).  

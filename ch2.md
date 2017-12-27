# Stability

Have you ever noticed that the incidents that blow up into the biggest issues start with something very small? A tiny programming error starts the snowball rolling downhill.

In any incident, my first priority is always to restore service. Restoring service takes precedence over investigation. If I can collect some data for post-mortem root cause analysis, that’s great—unless it makes the outage longer.

A post-mortem is like a murder mystery. You have a set of clues. Some are reliable, such as server logs copied from the time of the outage. Some are unreliable, such as statements from people about what they saw. As with real witnesses, people will mix observations with speculation. They will present hypotheses as facts. 

A better question to ask is, “How do we prevent bugs in one system from affecting everything else?” Inside every enterprise today is a mesh of interconnected, interdependent systems. They cannot—must not—allow bugs to cause a chain of failures. You’re going to look at design patterns that can prevent this type of problem from spreading.


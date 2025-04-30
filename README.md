[![Sigma CI](https://github.com/KeyboardGrunt/CyberOTC/actions/workflows/sigma-ci.yml/badge.svg)](https://github.com/KeyboardGrunt/CyberOTC/actions/workflows/sigma-ci.yml)
# CyberOTC
Personal training documentation for posterity, portfolio, and perhaps minimal public value.

This is a place where I show my work and progress over time as I train to become a stronger cyber security professional.

In time this repo may even provide value to someone.

## Repo layout
/detections/sigma/<rules>.yml<br>
/detections/yara/<rules>.yar<br>
/malware_sample_dumps/<threat_actor>/<dump>.md<br>
/scripts/ (helper Python/Go)<br>/docs/ (PDF reports, READMEs)<br>

## Planned future work
I'm currently writing Sigma rules based on threat reports I read as I go. They are with the greatest likelihood duplicates of existing rules that should come as a default detection for any modern SIEM solution. I'm aware. The point of this repo is documenting my progression, and I want to be able to churn out lint-passing Sigma rules with my eyes closed one day.

The sigma linter workflow ensures that all sigma rules can be safely converted to my desired search language and antagonistically integrated to whichever platform I end up using in the future. Right now I'm working with a lightweight ELK stack and the next significant step is to get the continuous delivery part of the chain going. I should be able to write a new sigma rule on my private wowrkstation, push it to github and have it verified, translated into ES|QL, and implemented as a detection rule in my ELK stack.

I'm also working on a vulnerability exposure workflow where I can dynamically get an asset inventory of my home lab, feed the results to an OpenVAS scanner, scan for vulnerabilities, and enrich those results with context data in one automated flow.

# Bitbucket Server Nexus IQ for SCM Integration

### Issue: Pull request, commit feedback, Code Insight not working 

#### Observations:
1. All configurations are done according to [this guide](https://help.sonatype.com/integrations/nexus-iq-for-scm/source-control-configuration).
2. Pull request, commit feedback and Code Insight are not working.
3. Connection between IQ Server and Bitbucker Server are open. Test with `ping` and `telnet`.
3. No obvious error in the log.

#### Cause:
Bitbucket Server version might not be compatible. Nexus IQ for SCM requires Bitbucket Server 6.7 and above. 

#### Solution:
Upgrade Bitbucket Server.

#### Result:
Pull request, commit feedback and Code Insight are working.

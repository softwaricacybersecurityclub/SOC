**Events**: Any observable cccurrence in a system or network.
___
**Alerts**: An event of interest that may be unwanted or unauthorized.
___
**Incidents**: A voilation or imminent threat of violation of computer security policies, acceptable use policies, or standerd security practices.
___

## Event Collection
Most logs are records of Event transaction data.
fig-1 the example of logs these can be important as well as unecessary but is recorded because it can be important in future.

![[Pasted image 20221016100508.png]]
*fig-1*

### Event log flow
Network events and endpoint events are recorded as logs in SIEM. These logs are then analyse with rules and according to rules logs are seperated into alerts or only events.
![[Pasted image 20221016100912.png]]
*fig-2*

`Qn- Collecting lots of events is great for detection?`

Things to be consider before collecting it:
* SIEMs are licensedd on volume and EPS
* Searching more data takes longer
* Finding signal is harder in the noise

`Goal of soc is tactical detection, not hoarding.`


# Complete cron for ZurmoCRM - v2.0.18
#
# <min> <hour> <day-month> <month> <week> $uSER cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO <job> &> /dev/null
# <0-60> <0-23> <0-31>     <1-12>  <0-6>  
#

USER_SYS=root
USER_ZURMO=super
FOLDER=/path/to/zurmo

# Every 1 minute
*/1 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO ProcessOutboundEmail &> /dev/null

# Every 2 minutes
*/2 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO Export &> /dev/null

# Every 5 minutes
*/5 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO EmailArchiving &> /dev/null
*/5 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO EmailBounce &> /dev/null
*/5 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO Monitor &> /dev/null

# Every 15 minutes
*/15 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO ByTimeWorkflowInQueue &> /dev/null
*/15 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO WorkflowMessageInQueue &> /dev/null

# Every 30 minutes
*/30 * * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO AddressGeocodeUpdate &> /dev/null

# Every 1 hour
* 0-23/1 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO AutoresponderQueueMessagesInOutbox &> /dev/null
* 0-23/1 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO CampaignGenerateDueCampaignItems &> /dev/null
* 0-23/1 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO CampaignMarkCompleted &> /dev/null
* 0-23/1 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO CampaignQueueMessagesInOutbox &> /dev/null

# 1x per day
30 4 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO ClearSentNotificationsEmail &> /dev/null
30 4 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO TestOutboundEmail &> /dev/null
20 12 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO JobLogCleanup &> /dev/null
30 4 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO WorkflowValidityCheck &> /dev/null
30 4 * * * $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO CurrencyRatesUpdate &> /dev/null

# 1x per week
30 3 * * 6 $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO ExportCleanup &> /dev/null
30 3 * * 6 $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO ImportCleanup &> /dev/null
30 3 * * 6 $USER_SYS cd $FOLDER/app/protected/commands && ./zurmoc jobManager $USER_ZURMO CheckZurmoUpdates &> /dev/null

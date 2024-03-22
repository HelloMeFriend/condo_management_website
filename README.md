# classprogressreport-yo
classprogressreport-yo created by GitHub Classroom <br />
Minh Duc Vu - 40166824 <br />
Omar Alshanyour - 40209637 <br />
1. 
```
data class ReadingTime(
	val minutes: Int,
	val hours: Int,
	val isContinue: Boolean,
) {

	fun format(resources: Resources): String = when {
		hours == 0 && minutes == 0 -> resources.getString(R.string.less_than_minute)
		hours == 0 -> resources.getQuantityString(R.plurals.minutes, minutes, minutes)
		minutes == 0 -> resources.getQuantityString(R.plurals.hours, hours, hours)
		else -> resources.getString(
			R.string.remaining_time_pattern,
			resources.getQuantityString(R.plurals.hours, hours, hours),
			resources.getQuantityString(R.plurals.minutes, minutes, minutes),
		)
	}
}

```
a) The inputs for this function are: resources, [hours, minutes, and isContinue] --> global variables <br />
b) <br />
	*i) The paritions are [resources is null] and [resources isn't null]    <br />
Vithujanan Vigneswaran - 40157822<br />
Jackson Jean - 23507416

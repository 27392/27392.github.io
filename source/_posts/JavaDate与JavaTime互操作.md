---
title: JavaDate与JavaTime互操作
date: 2020-06-30 18:27:33
tags:
---

|  类   | 遗留类 | 转换到遗留类 | 转换自遗留类|
|  ----  | ----  |----  |----  |
| Instant  | java.util.Date |Date.form(instant)| data.toInstant()|
| ZonedDateTime  | java.util.GregorianCalendar |GregorianCalendar.form(zonedDateTime)| gregorianCalendar.toZonedDateTime()|
| Instant  | java.sql.Timestamp |Timestamp.form(instant)| timestamp.toInstant()|
| LocalDateTime  | java.sql.Timestamp |Timestamp.valueOf(localDateTime)| timestamp.toLocalDateTime()|
| LocalDate  | java.sql.Date |Date.valueOf(localDate)| data.toLocalDate()|
| LocalTime  | java.sql.Time |Time.valueOf(localDataTime)| time.toLocalTime()|
| DateTimeFormatter  | java.text.DateFormat |dateTimeFormatter.toFormat()| 无|
| ZoneId  | java.util.TimeZone |Timezone.getTimeZone(zoneId)| timeZone.toZoneId()|
| Instant  | java.not.file.attribute.FileTime |FileTime.from(instant)| fileTime.toInstant()|
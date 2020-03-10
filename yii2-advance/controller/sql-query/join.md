# ตัวอย่าง Join

```php
$meetingRoom = MeetingRoom::find()
            ->select([
                'meeting_room.id as meeting_room_id',
                'meeting_room.name as meeting_room_name',
                'meeting_room.layouts as meeting_room_layouts',
                'meeting_room.capacity as meeting_room_capacity',
                'meeting_room.room_status as meeting_room_room_status',

                'booking.meeting_room_id as booking_meeting_room_id',
                'booking.start_time as booking_start_time',
                'booking.end_time as booking_end_time',
            ])
            ->leftJoin('booking', 'booking.meeting_room_id = meeting_room.id')
            ->where([
                'meeting_room.status' => 'active',
            ])
            ->orderBy(['meeting_room.name' => 'SORT_ASC'])
            // ->distinct()
            ->limit(5)
            ->asArray()
            ->all();
```


# ตัวอย่าง Join

```php
use yii\db\Query;

$meetingRoom = (new Query())
            ->select([
                'meeting_room.id as meeting_room_id',
                'meeting_room.name as meeting_room_name',
                'meeting_room.image as meeting_room_image',
                'meeting_room.capacity as meeting_room_capacity',
                'meeting_room.room_status as meeting_room_room_status',

                'booking.meeting_room_id as booking_meeting_room_id',
                'booking.start_time as booking_start_time',
                'booking.end_time as booking_end_time',
            ])
            ->from('meeting_room')
            ->leftJoin('booking', 'booking.meeting_room_id = meeting_room.id')
            ->where([
                'meeting_room.status' => 'active',
            ])
            ->orderBy(['name' => 'SORT_ASC'])
            ->distinct()
            ->limit(5)
            ->all();
```


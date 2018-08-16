item_entity.lua replacement

edited by TenPlus1

Features:
- Items are destroyed by lava
- Items are pushed along by flowing water (thanks to QwertyMine3)
- Items are removed after 900 seconds or the time that is specified by
   remove_items in minetest.conf (-1 disables it)
- Particle effects added
- Dropped items slide on nodes with {slippery} groups
- Items stuck inside solid nodes move to nearest empty space
- Added 'dropped_step(self, pos, dtime)' custom on_step for dropped items
   'self.node_inside' contains node table that item is inside
   'self.def_inside' contains node definition for above
   'self.node_under' contains node table that is below item
   'self.def_under' contains node definition for above
   'self.age' holds age of dropped item in seconds
   'self.itemstring' contains itemstring e.g. "default:dirt", "default:ice 20"
   'pos' holds position of dropped item
   'dtime' used for timers

   return false to skip further checks by builtin_item

License: MIT

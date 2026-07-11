**Engine config**
- pygame.mixer.init()  
- pygame.mixer.get_init() -> bool  
- pygame.mixer.quit()

**Music stream**
- pygame.mixer.music.load(path)
- pygame.mixer.music.play()
- .stop()
- .pause()
- .unpause()
- .fadeout()
- .get_busy()
- .set_volume(int) # Btw 0 and 1
- .get_volume()
- .get_length() # Seconds

**Channels config**
- pygame.mixer.set_num_channels(int) # All have id like an index
- pygame.mixer.get_num_channels() # Total number of channels
- .set_reserved(int)
- .find_channel() # Returns a channel object if free

**Global config**
- .get_busy()
- .stop()
- .pause()
- .unpause()
- .fadeout()

**Channel Object** 
- channel = pygame.mixer.Channel(id/index)
- .play(sound object)
- .stop()
- .pause()
- .unpause()
- .fadeout()
- .set_volume() # Btw 0 and 1
- .get_volume()
- .get_busy()
- .get_sound() # get the current playing sound
- .queue(Sound object) # queue a Sound object to follow the current
- Each channel can only have a single sound queued to it at a time
- .get_queue() # return any sound that is queued on the channel
- .set_endevent() # have a channel send an event when playack stops
- .get_endevent() # get the event a channel sends when playback stop

**Sound object**
- sound = pygame.mixer.Sound(path)
- .play()
- .stop()
- .fadeout()
- .set_volume()
- .get_volume()
- .get_num_channels() # returns the number of active channels this sound is playing on
- .get_length()

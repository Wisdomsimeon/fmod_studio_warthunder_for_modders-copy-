## BY USING THIS CONTENT YOU AGREE TO THE FOLLOWING CONTRIBUTION AGREEMENT

https://live.warthunder.com/contribution_agreement/?lang=en

This repository contains the Fmod Studio project for War Thunder. This project allows you to create sound modifications. The project doesn’t include crew chat, other monologues, and music. To save space, assets are compressed into vorbis format in the .ogg container (extensions renamed to .wav to preserve the integrity of the original sound event). To keep the project work in the game you shouldn't change sound events names, and the structure of their location in the project.  Also, do not change the structure of the mixer buses.

Actual Fmod Studio version - 2.1.6

Important notice:
In this repository we added compressed assets (with losses, ogg, vorbis) in order to decrease the size of repository (originally over 20 Gb). This project is intended to use with not compressed assets (wav, 44100 Hz, 16bit for example), because it has global compression settings (vorbis, 37% quality). If compressed again, already compressed assets will loose sound quality a lot, and may sound with audible metallic overtone.

## ИСПОЛЬЗУЯ ДАННЫЕ МАТЕРИАЛЫ, ВЫ СОГЛАШАЕТЕСЬ СО СЛЕДУЮЩИМ СОГЛАШЕНИЕМ О ПРЕДОСТАВЛЕНИИ КОНТЕНТА

https://live.warthunder.com/contribution_agreement/?lang=ru

Данный репозиторий содержит проект Fmod Studio для игры War Thunder. На его основе можно создавать звуковые модификации. В проект не включены реплики экипажей, прочие монологи, музыка. Ассеты, в целях экономии места, сжаты в формат vorbis в контейнере ogg (расширения переименованы в wav для сохранения целостности исходного звукового ивента). Для работоспособности проекта в игре не надо менять имена звуковых ивентов, и структуру их расположения в проекте. Так же не надо менять структуру шин микшера.

Актуальная версия Fmod Studio - 2.1.6

Важно:
В репозиторий добавлены ассеты, сжатые с потерями (ogg, vorbis).  Это сделано для того, чтобы уменьшить объем ассетов, в не сжатом виде он превышает 20 Гб. То есть проект предназначен для работы с не сжатыми ассетами (wav, например 44100 Гц, 16 бит), поскольку в нем выставлены глобальные настройки сжатия (vorbis, качество 37%). Повторно сжатые ассеты сильно теряют в качестве, и могут звучать с заметным металлическим призвуком.

Patch notes:
--------------------------------------------------------------------------------------------------------
-----------------------
17.09.2021 - Direct Hit fmod project update.
----------------------------------

This update got the new automatic weapon sound system, and new automatic weapon sound events, for all in-game vehicles. In a nutshell, it is a kind of loop mode, but with an element of a granular synthesis. You can read about how you can switch the support of sound modification between old and new weapon sound systems here:

EN:
https://wiki.warthunder.com/Sound_modifications

RU:
https://wiki.warthunder.ru/%D0%97%D0%B2%D1%83%D0%BA%D0%BE%D0%B2%D1%8B%D0%B5_%D0%BC%D0%BE%D0%B4%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D0%B8

-----------------------
18.06.2021 - Red Skies fmod project update.
----------------------------------

The main feature of this update - there is no more hangar.bank, all sound events distributed between other fmod banks (make sure you have no old hangar.bank in your mod folder, it can lead to random consequences, like super-loud sounds). Also, now we have more ground vehicles tracks sound events, and several new sound events, like pjojectiles camera for naval battles, ground vehicles suspension hits, etc.

-----------------------
30.03.2021 - Added custom script for weapon rapid fire tests.
----------------------------------

Now you can try rapid fire with "Ctrl+," shortcut. Update fmod project and run Script->Reload menu command. Then, choose weapon sound event that contains on_shot parameter, press Play, and hit "Ctrl+,". You also will be able to adjust fire rate from 0 to 2000 rpm.

-------------------------------------------------------------------------------------------------------------------------------
24.03.2021 - Ixwa Strike project update.
----------------------------------

The main feature of this project is aircraft weapon sound generation system, now it is oneshot instead of looping mode. But, still you can switch between looping and oneshot system, by typing useLoopsForGunSound:b=yes in sound{} block of config.blk.

PS: hangar.bank still contains music events, that's bad news. But, I'm about to get rid of it in the next major update.

----------------------------------
25.12.2020 - Fmod Studio project version changed to 2.1.6.
-------------------------------------------------------------------------------------------------------------------------------
High fire rate weapon sound events forming method changed from loop to one shot.
Note: now you can choose automatic weapon sound events forming method (loop/oneshot) by adding in config.blk in sound{} block this string: useLoopsForGunSound:b=yes

27.11.2020 - Fmod Studio project updated to "New Power" release state.
-------------------------------------------------------------------------------------------------------------------------------
16.07.2020 - Fmod Studio version updated. Now it is 2.00.09.
-------------------------------------------------------------------------------------------------------------------------------
New dialog localisations (assets) will be added gradually with next commits.
-------------------------------------------------------------------------------------------------------------------------------
09.04.2020 - Added fmod project version related to major patch 1.97.1.X

Fmod Studio version - 1.10.17

 - Weapon system reworked, added "on_shot" parameter that triggers shot event. That was done for better sound channels control.
 - Explosions and cannons gain a modular assembly system.
 - Added crew dialogs, all languages for ground and naval crew, aircraft crew - only english and russian (for now).
 - Added empty music events

Notes:
music events in aircraft/music/init should be empty, do not add any music in these events.
-------------------------------------------------------------------------------------------------------------------------------
SET( MUSIC_FILES
     BoosterMusicBooks.zip

)

ADD_CUSTOM_TARGET(music ALL DEPENDS ${MUSIC_FILES})

IF (UNIX AND NOT APPLE)
    INSTALL( FILES ${MUSIC_FILES} DESTINATION share/games/pianobooster/music )
ENDIF (UNIX AND NOT APPLE)

IF (WIN32)
    INSTALL( FILES ${MUSIC_FILES} DESTINATION . )
ENDIF (WIN32)

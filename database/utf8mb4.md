# utf8mb4

`set character_set_client = 'utf8mb4'`

글 본문에 이모지가 포함되어있을땐 글자 인코딩을 확인합시다! utf8mb4로 되어있어야지만 이모지가 가능합니다.

`ALTER TABLE table_name convert to charset utf8mb4;`


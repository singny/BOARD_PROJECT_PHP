```
CREATE TABLE BOARD_CONTENTS 
(
  CON_NO NUMBER(5, 0) NOT NULL 
, CON_DATETIME VARCHAR2(30 BYTE) NOT NULL 
, WR_USER NUMBER(10, 0) NOT NULL 
, CON_TITLE VARCHAR2(30 BYTE) NOT NULL 
, CON_BODY VARCHAR2(100 BYTE) NOT NULL 
, RE_USER NUMBER(10, 0) NOT NULL 
, CON_VC NUMBER(10, 0) 
, CONSTRAINT PK_CON PRIMARY KEY 
  (
    CON_NO 
  )
  USING INDEX 
  (
      CREATE UNIQUE INDEX PK_CON ON BOARD_CONTENTS (CON_NO ASC) 
      LOGGING 
      TABLESPACE EXERCISE3 
      PCTFREE 10 
      INITRANS 2 
      STORAGE 
      ( 
        INITIAL 65536 
        NEXT 1048576 
        MINEXTENTS 1 
        MAXEXTENTS UNLIMITED 
        BUFFER_POOL DEFAULT 
      ) 
      NOPARALLEL 
  )
  ENABLE 
) 
LOGGING 
TABLESPACE EXERCISE3 
PCTFREE 10 
INITRANS 1 
STORAGE 
( 
  INITIAL 65536 
  NEXT 1048576 
  MINEXTENTS 1 
  MAXEXTENTS UNLIMITED 
  BUFFER_POOL DEFAULT 
) 
NOCOMPRESS 
NOPARALLEL;
```

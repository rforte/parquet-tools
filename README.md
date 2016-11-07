Usage
============
Example of dumping the schema of a parquet file:
```
Nicks-MacBook-Pro:parquet-tools rforte$ ./parquet-schema ~/s3/wmt/part-r-00000-36534b35-7051-4221-8fbf-58a0ffa5a510.gz.parquet
message spark_schema {
  optional binary clientIp (UTF8);
  optional binary redirectIp (UTF8);
  optional group ipChain (LIST) {
    repeated group list {
      optional binary element (UTF8);
    }
  }
  optional binary hmguid (UTF8);
  optional int64 requestTime;
  optional group queryString (MAP) {
    repeated group key_value {
      required binary key (UTF8);
      optional binary value (UTF8);
    }
  }
  optional int32 returnCode;
  optional int32 size;
  optional binary referer (UTF8);
  optional binary userAgent (UTF8);
  optional binary pid (UTF8);
  optional int32 dupeCount;
  optional binary type (UTF8);
  optional group annotations (MAP) {
    repeated group key_value {
      required binary key (UTF8);
      optional group value (LIST) {
        repeated group list {
          optional binary element (UTF8);
        }
      }
    }
  }
  optional group tags (LIST) {
    repeated group list {
      optional binary element (UTF8);
    }
  }
  optional binary beaconId (UTF8);
  optional binary action (UTF8);
  optional int64 bornTime;
  optional group parsedUserAgent (MAP) {
    repeated group key_value {
      required binary key (UTF8);
      optional binary value (UTF8);
    }
  }
  optional binary beaconSourceType (UTF8);
  optional binary mediaSourceId (UTF8);
  optional binary reqdate (UTF8);
  optional binary reqhour (UTF8);
}
```

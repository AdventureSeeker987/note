

## golang orm update field 


if you have a int field in your struct, when you use orm framework to update your entity in db like `Status`

```go
type Entity struct {
	JobName       string            `json:"job_name,omitempty"`
	SourceTable   string            `json:"source_table,omitempty"`
	Status        int               `json:"status,omitempty"`
}
```


Update func:
```go
funcUpdate(ctx context.Context, record *T) (sql.Result, error) {
	res, err := r.db.NewUpdate().
		Model(record).
		OmitZero().
		WherePK().
		Exec(ctx)
}
```

if you use status=0 to stand for some meanful status like failure, It will be omitted by Update()

## solution

1. change Status type; not use int(default value:0) to express status
2. define your one status like -1:failure 

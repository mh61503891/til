# ActiveRecord

## Using SQLite3 in memory

```ruby
ActiveRecord::Base.establish_connection(
   adapter: 'sqlite3', database: ':memory:'
)
```

```ruby
ENV['DATABASE_URL'] = 'sqlite3::memory:'
ActiveRecord::Base.establish_connection(ENV['DATABASE_URL'])
```


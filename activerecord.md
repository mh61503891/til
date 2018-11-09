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

## Migration

```ruby
ActiveRecord::Schema.define do
  if !table_exists?(:people)
    create_table :people do |t|
      t.string :uid
      t.string :name
    end
    add_index :people :uid, unique: true
    add_index :people :name
  end
end
```

## Hints

* ` DATABASE_URL` に日本語が含まれるとURIクラスの `rfc2396_parser.rb` で `URI::InvalidURIError` がスローされる。
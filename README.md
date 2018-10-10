### fabrication
---
https://github.com/paulelliott/fabrication
https://www.fabricationgem.org/

```ruby
class Person < ActiveRecord::Base
  belongs_to :neighborhood
  has_many :houses
end

Fabricator(:person) do
  neighborhood
  houese(count: 2)
  name { Faker::Name.name }
  age 45
  gender { %w(M F).sample }
end

Fabricate(:person, name: 'Paul Elliott', gender: 'M') do
  houses { [Fabricate(:house, location: 'the beach')] }
end






```


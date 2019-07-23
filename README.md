### Gab
---
https://code.gab.com/gab/social/gab-social/

```rb
// spec/rails_helper.rb

RSpec::Sidekiq.configure do |config|
  config.warn_when_jobs_not_processed_by_sidekiq = false
end

def request_fixture(name)
  File.read(Rails.root.join('spec', 'fixtures', 'requests', name))
end

def attachment_fixture(name)
  File.open(Rails.root.join('spec', 'fixtures', 'files', name))
end

def stub_jsonld_contexts!
  stub_request(:get, 'https://www.w3.org/ns/activitystreams').to_return(request_fixture('json-ld.activitystreams.txt'))
  stub_request(:get, 'https://w3id.org/identity/v1').to_return(request_fixture('json-ld.identity.txt'))
  stub_request(:get, 'https://w3id.org/security/v1').to_return(request_fixture('json-ld.security.txt'))
end

```

```
BTCPAY_LEGACY_TOKEN
BTCPAY_PUB_KEY
BTCPAY_MERCHANT_TOKEN
```

```
```


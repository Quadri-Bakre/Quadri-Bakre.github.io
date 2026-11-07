source "https://rubygems.org"

# Same Jekyll version on the Mac, the Windows PC and GitHub
gem "jekyll", "~> 4.4"

# Windows needs time zone data that Mac and Linux already have
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

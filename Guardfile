# Project Guardfile
# More info at https://github.com/guard/guard#readme

group :red_green_refactor, halt_on_fail: true do
  
  guard :rubocop do
    watch(/.+\.rb$/)
    watch('.rubocop.yml') { |m| File.dirname(m[0]) }
  end

  guard :rails, port: 3000, host: '0.0.0.0' do
    watch('Gemfile.lock')
    watch(%r{^(config|lib)/.*})
  end
end

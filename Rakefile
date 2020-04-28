task default: %w[serve]

task :serve do
  sh "bundle exec jekyll serve"
end

task :deploy do
  sh "JEKYLL_ENV=production bundle exec jekyll build"
  sh "aws s3 cp --recursive _site/ s3://www.comocovid.com/"
end

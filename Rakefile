require 'vidazing_logger'

NAME = "VidaZing"

log = VidazingLogger.logger

task :default => ["build"]

desc "Builds #{NAME}"
task :build, :release do |t, args|
  if args.has_key?(:release)
    log.info "Setting build env 'JEKYLL_ENV=production'"
    build_envs ='JEKYLL_ENV=production '
  end

  log.info "Building #{NAME}"
  system("#{build_envs}bundle exec jekyll build")
end


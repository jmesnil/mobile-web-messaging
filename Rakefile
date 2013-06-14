require 'rubygems'
require 'bundler/setup'

require 'asciidoctor'
require 'rake/clean'

CLEAN.include 'output/'

task :default => :build

desc "Build the doc"
task :build do
  Dir.mkdir 'output' unless File.directory? 'output'
  Dir.glob('*.asciidoc').select do |fn| 
    Asciidoctor.render_file fn, :to_dir => 'output'
  end
end


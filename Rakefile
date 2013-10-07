# -*- ruby -*-
require 'rubygems'
require 'hoe'
require 'rake/extensiontask'

Hoe.plugin :bundler, :rubygems, :doofus, :git, :minitest

Hoe.spec 'diff_match_patch_native' do
  developer('Elliot Laster', 'elliotlaster@gmail.com')
  self.version = '1.0.1'
  self.readme_file   = 'README.rdoc'
  self.history_file  = 'History.txt'
  self.extra_dev_deps << ['rake-compiler', '>= 0']

  self.spec_extras = { :extensions => ["ext/diff_match_patch/extconf.rb"] }

  Rake::ExtensionTask.new('diff_match_patch', spec)
end

Rake::Task[:test].prerequisites << :compile

---
layout: post
title: "Carrierwave image quality"
description: ""
category:
tags: [tech, ruby]
---
{% include JB/setup %}

[Carierwave](https://rubygems.org/gems/carrierwave) is an awesome gem to manage your uploads. It is pure Ruby, so it isn't strangled in Rails or ActiveRecord.
It is easy configurable, but I missed one option.

It doesn't support to change the quality of your uploade images.
But if you use RMagick or MiniMagick, you can use this snippet.

    # rails carrierwave initializer that gives you a quality option in your uploader. use:
    #  version :medium do
    #    process :resize_to_fit => [640, 480]
    #    process :quality => 95
    #  end

    module CarrierWave
      module MiniMagick
        def quality(percentage)
          manipulate! do |img|
            img.write(current_path){ self.quality(percentage) }
            img = yield(img) if block_given?
            img
          end
        end
      end
    end

If you are using RMmagick, just replace self.quality(percentage) with self.quality = percentage.
With thanks to [matwiemann](https://gist.github.com/matwiemann) for [sharing this solution](https://gist.github.com/730273/50b9ced7db199f1ede2d79eb78e844053d2060ee)

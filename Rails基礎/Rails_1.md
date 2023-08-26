###ジェネレーターの設定  
- 記述する所＝＞**config/application.rb**
    
    ```ruby
    config.generators do |g|
      # デフォルトのORMを設定（例：:active_record、:mongoidなど）
      g.orm :active_record
    
      # デフォルトのテストフレームワークを設定（例：:test_unit、:rspecなど）
      g.test_framework :rspec, fixture: false
    
      # デフォルトのビューテンプレートエンジンを設定（例：:erb、:hamlなど）
      g.template_engine :erb
    
      # ビュー関連のファイル（ビュー、ヘルパー、スタイルシート）を生成しない
      g.assets false
    
      # ヘルパーファイルを生成しない
      g.helper false
    
      # マイグレーションファイルを生成しない
      g.skip_migration true
    end
    ```
    
    上記config.generators do |g|〜endの中に必要なオプションを記載
    
    特定のジェネレーターのコマンドでオプションを指定した場合、そのコマンドのオプションが優先されることに注意
    
    ```ruby
    config.generators do |g|
      g.helper false
      g.test false
      g.skip_routes true
    end
    ```
    
    [コマンドラインツール - Railsガイド](https://railsguides.jp/command_line.html#rails-generate)
    
    ## 書く所の詳細
    
    1. ファイルは**config/application.rb**
    2. 下記のようにApplicationクラスの中に記載する
    
    ```ruby
    module V3BasicRailsBasic
      class Application < Rails::Application
        # Initialize configuration defaults for originally generated Rails version.
        config.load_defaults 7.0
        config.generators do |g|
          g.helper false
          g.test false
          g.skip_routes true
        end
        # Configuration for the application, engines, and railties goes here.
        #
        # These settings can be overridden in specific environments using the files
        # in config/environments, which are processed later.
        #
        # config.time_zone = "Central Time (US & Canada)"
        # config.eager_load_paths << Rails.root.join("extras")
    
        # Don't generate system test files.
        config.generators.system_tests = nil
      end
    end
    ```
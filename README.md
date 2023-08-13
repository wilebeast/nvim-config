# nvim-config
use { "neovim/nvim-lspconfig",
      config = get_config("lsp"),
      require('lspconfig').gopls.setup{
          cmd = {"gopls", "serve"},  -- �~L~G�~Z gopls �~Z~D�~Q�令为 "gopls serve"
          settings = {
              gopls = {
                  analyses = {
                      unusedparams = true,  -- �~P��~T��~\�使�~T��~O~B�~U��~Z~D�~H~F�~^~P
                  },
                  staticcheck = true,  -- �~P��~T��~]~Y�~@~A�~@�~_�
              },
          },
     }
}

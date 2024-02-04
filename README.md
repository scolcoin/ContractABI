# Gestión de Token
Este espacio esta diseñado para que todos los proyectos que quieran integrar la wallet de scolcoin deben ingresar su contrato.sol y su ABI.
Nota: con esto se podra operar el token.

`token/`

Ejemplo:
- scolcoin.sol
- scolcoin.abi
- scolcoin.txt


`nft/`

Ejemplo:
- scolnft.sol
- scolnft.abi
- scolnft.txt

## El Archivo TXT

debe contener ejemplo:

`{

  "message": "OK",
  
  "result": {
  
    "cataloged": true,
    
    "contractAddress": "0xcc8552943da009a3b0757bf02dafbdf5e8c8fba4",
    
    "decimals": "18",
    
    "name": "EWATTS",
    
    "symbol": "EWG",
    
    "totalSupply": "1100000000000000000000000",
    
    "type": "ERC-20"
    
  },
  "status": "1"
}`

## El Archivo ABI

Recuerden que un ABI debe tener este formato ejemplo:
`[{"inputs":[{"internalType":"string","name":"_nombre","type":"string"},{"internalType":"string","name":"_ccoNit","type":"string"},{"internalType":"string","name":"_email","type":"string"},{"internalType":"string","name":"_indicativo","type":"string"},{"internalType":"string","name":"_celular","type":"string"},{"internalType":"string","name":"_nickname","type":"string"},{"internalType":"address","name":"_wallet","type":"address"},{"internalType":"bool","name":"_user_auto","type":"bool"}],"name":"agregarUsuario","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"_vps","type":"address"},{"internalType":"string","name":"_empresa","type":"string"},{"internalType":"bool","name":"_vps_auto","type":"bool"}],"name":"agregarVPS","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"_usuario","type":"address"},{"internalType":"bool","name":"nuevoEstadoAutoUsuario","type":"bool"}],"name":"modificarEstadoAutoUsuario","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"_vps","type":"address"},{"internalType":"bool","name":"nuevoEstadoAutoVPS","type":"bool"}],"name":"modificarEstadoAutoVPS","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"string","name":"_nombre","type":"string"},{"internalType":"string","name":"_ccoNit","type":"string"},{"internalType":"string","name":"_email","type":"string"},{"internalType":"string","name":"_indicativo","type":"string"},{"internalType":"string","name":"_celular","type":"string"},{"internalType":"string","name":"_nickname","type":"string"},{"internalType":"address","name":"_wallet","type":"address"}],"name":"modificarUsuario","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"_usuario","type":"address"},{"internalType":"address","name":"nuevaWallet","type":"address"}],"name":"modificarWalletUsuario","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"_vps","type":"address"},{"internalType":"address","name":"nuevaWalletVPS","type":"address"}],"name":"modificarWalletVPS","outputs":[],"stateMutability":"nonpayable","type":"function"},{"anonymous":false,"inputs":[{"indexed":true,"internalType":"address","name":"previousOwner","type":"address"},{"indexed":true,"internalType":"address","name":"newOwner","type":"address"}],"name":"OwnershipTransferred","type":"event"},{"inputs":[],"name":"renounceOwnership","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"newOwner","type":"address"}],"name":"transferOwnership","outputs":[],"stateMutability":"nonpayable","type":"function"},{"anonymous":false,"inputs":[{"indexed":false,"internalType":"bool","name":"existe","type":"bool"}],"name":"UsuarioExistente","type":"event"},{"anonymous":false,"inputs":[{"indexed":false,"internalType":"bool","name":"existe","type":"bool"}],"name":"UsuarioExistentePorCcoNit","type":"event"},{"anonymous":false,"inputs":[{"indexed":false,"internalType":"bool","name":"existe","type":"bool"}],"name":"UsuarioExistentePorEmail","type":"event"},{"anonymous":false,"inputs":[{"indexed":false,"internalType":"bool","name":"existe","type":"bool"}],"name":"UsuarioExistentePorNickname","type":"event"},{"anonymous":false,"inputs":[{"indexed":true,"internalType":"address","name":"vps","type":"address"},{"indexed":false,"internalType":"address","name":"nuevaWalletVPS","type":"address"}],"name":"UsuarioModificado","type":"event"},{"inputs":[],"name":"verificarYEnviarEventos","outputs":[],"stateMutability":"nonpayable","type":"function"},{"inputs":[{"internalType":"address","name":"_wallet","type":"address"}],"name":"encontrarUsuario","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"_vpsAddress","type":"address"}],"name":"isVPS","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"numusuario","outputs":[{"internalType":"uint256","name":"","type":"uint256"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"_userId","type":"uint256"}],"name":"obtenerDatosUsuarioPorId","outputs":[{"components":[{"internalType":"uint256","name":"id","type":"uint256"},{"internalType":"string","name":"nombre","type":"string"},{"internalType":"string","name":"ccoNit","type":"string"},{"internalType":"string","name":"email","type":"string"},{"internalType":"string","name":"indicativo","type":"string"},{"internalType":"string","name":"celular","type":"string"},{"internalType":"string","name":"nickname","type":"string"},{"internalType":"address","name":"wallet","type":"address"},{"internalType":"bool","name":"user_auto","type":"bool"}],"internalType":"struct Usuarios.Usuario","name":"","type":"tuple"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"_vpsWallet","type":"address"}],"name":"obtenerNombreVPSPorWallet","outputs":[{"internalType":"string","name":"","type":"string"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"_userId","type":"uint256"}],"name":"obtenerUsuario","outputs":[{"components":[{"internalType":"uint256","name":"id","type":"uint256"},{"internalType":"string","name":"nombre","type":"string"},{"internalType":"string","name":"ccoNit","type":"string"},{"internalType":"string","name":"email","type":"string"},{"internalType":"string","name":"indicativo","type":"string"},{"internalType":"string","name":"celular","type":"string"},{"internalType":"string","name":"nickname","type":"string"},{"internalType":"address","name":"wallet","type":"address"},{"internalType":"bool","name":"user_auto","type":"bool"}],"internalType":"struct Usuarios.Usuario","name":"","type":"tuple"}],"stateMutability":"view","type":"function"},{"inputs":[],"name":"owner","outputs":[{"internalType":"address","name":"","type":"address"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"string","name":"_ccoNit","type":"string"}],"name":"usuarioExistePorCcoNit","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"string","name":"_email","type":"string"}],"name":"usuarioExistePorEmail","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"uint256","name":"_userId","type":"uint256"}],"name":"usuarioExistePorId","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"string","name":"_nickname","type":"string"}],"name":"usuarioExistePorNickname","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"_wallet","type":"address"}],"name":"usuarioExistePorWallet","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"},{"inputs":[{"internalType":"address","name":"_vps","type":"address"}],"name":"vpsExistePorWallet","outputs":[{"internalType":"bool","name":"","type":"bool"}],"stateMutability":"view","type":"function"}]`

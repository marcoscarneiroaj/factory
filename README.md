# factory

Script standalone para Roblox com GUI movel e eventos configuraveis, pensado para um jogo separado.

## Rodar

```lua
loadstring(readfile("factory\\factory.lua"), "@factory\\factory.lua")()
```

Ou pelo GitHub Raw:

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/SEU_USUARIO/factory/main/factory.lua", true))()
```

## Evento atual

- `Manual Machine`: faz `game:GetService("ReplicatedStorage").Events.MachineClickEvent:FireServer("ManualMachine")` em loop.
- Botao na GUI para ligar e desligar.
- Tecla padrao: `F`.

## Como adicionar mais eventos

Abra `factory.lua` e adicione um novo bloco dentro da tabela `EVENTS`:

```lua
{
    Id = "nome_unico",
    Title = "Nome na GUI",
    Description = "Descricao do que o evento faz",
    ToggleKey = Enum.KeyCode.G,
    Delay = 0.15,
    Run = function()
        -- seu FireServer aqui
    end,
},
```

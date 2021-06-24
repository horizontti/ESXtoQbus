# ESXtoQbus
How to convert ESX to Qbus

<picture>
  <img src="https://img.aijaa.com/b/00969/14970800.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00272/14970801.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00159/14970802.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00091/14970803.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00297/14970804.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00843/14970805.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00574/14970806.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00714/14970807.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00346/14970808.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00135/14970809.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00891/14970810.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00131/14970811.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00448/14970812.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00662/14970813.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00728/14970814.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00767/14970815.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00550/14970816.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00249/14970817.jpg" style="width:auto;">
  <br>
  <img src="https://img.aijaa.com/b/00962/14970818.jpg" style="width:auto;">
  <br>
</picture>

esx:onPlayerDeath -> hospital:server:SetDeathStatus

esx:playerLoaded -> QBCore:Client:OnPlayerLoaded (use for setting a variable to let the script know the player is ready)

esx:showAdvancedNotification -> QBCore:Notify

esx:showHelpNotification -> QBCore:Notify

esx:showNotification -> QBCore:Notify

ESX.GetPlayerData -> QBCore.Functions.GetPlayerData

ESX.IsPlayerLoaded -> None (checks if player is loaded so not relevant)

ESX.SetPlayerData -> QBCore:Player:SetPlayerData

ESX.TriggerServerCallback -> QBCore.Functions.TriggerCallback

ESX.Game.DeleteObject -> None (Can use FiveM native DeleteEntity)

ESX.Game.DeleteVehicle -> QBCore.Functions.DeleteVehicle

ESX.Game.GetClosestObject -> None (Can use FiveM native GetClosestObjectOfType)

ESX.Game.GetClosestPed -> QBCore.Functions.GetClosestPed

ESX.Game.GetClosestPlayer -> QBCore.Functions.GetClosestPlayer

ESX.Game.GetClosestVehicle -> QBCore.Functions.GetClosestVehicle

ESX.Game.GetObjects -> None (uses enumeration)

ESX.Game.GetPedMugshot -> None (Can use FiveM native RegisterPedheadshot)

ESX.Game.GetPeds -> None (uses enumeration)

ESX.Game.GetPlayers -> QBCore.Functions.GetPlayers

ESX.Game.GetPlayersInArea -> None (uses enumeration)

ESX.Game.GetVehicleInDirection -> None (uses ray casting)

ESX.Game.GetVehicles -> QBCore.Functions.GetVehicles

ESX.Game.GetVehiclesInArea -> None (uses enumeration)

ESX.Game.IsSpawnPointClear -> None (uses getvehiclesinarea)

ESX.Game.SetVehicleProperties -> QBCore.Functions.SetVehicleProperties

ESX.Game.SpawnLocalObject -> None (dont bother)

ESX.Game.SpawnLocalVehicle -> None (dont bother)

ESX.Game.SpawnObject -> None (Can use FiveM Native CreateObject)

ESX.Game.SpawnVehicle -> QBCore.Functions.SpawnVehicle

ESX.Game.Teleport -> (Can use FiveM Native SetEntityCoords and SetEntityHeading)

ESX.Game.Utils.DrawText3D -> QBCore.Functions.DrawText3D

There is no direct translation for replacing ESX.Streaming or ESX.Scaleform or ESX.UI

ESX.CreatePickup -> None (irrelevant and done through qb-inventory)

ESX.GetItemLabel -> None (Just returns item label)

ESX.GetPlayerFromId -> QBCore.Functions.GetPlayer

ESX.GetPlayerFromIdentifier -> QBCore.Functions.GetPlayerByCitizenId

ESX.GetPlayers -> QBCore.Functions.GetPlayers

ESX.RegisterServerCallback -> QBCore.Functions.CreateCallback

ESX.RegisterUsableItem -> QBCore.Functions.CreateUseableItem

ESX.SavePlayer -> QBCore.Player.Save

ESX.SavePlayers -> None (dont bother)

ESX.Trace -> Use QBCore.Debug but dont bother converting this

ESX.UseItem -> QBCore.Functions.UseItem

xPlayer.removeWeaponComponent -> xPlayer.Functions.RemoveItem (component name)

xPlayer.setAccountMoney -> xPlayer.Functions.SetMoney (account)

xPlayer.setCoords -> None (used for teleporting)

xPlayer.setInventoryItem -> xPlayer.Functions.AddItem (item name)

xPlayer.setJob -> xPlayer.Functions.SetJob

xPlayer.setMaxWeight -> None (It is set in qb-core config) 

xPlayer.setMoney -> xPlayer.Functions.SetMoney

xPlayer.setName -> None (dont bother)

xPlayer.setWeaponTint -> None (qb-weapons does this)

xPlayer.showHelpNotification -> TriggerClientEvent('QBCore:Notify')

xPlayer.showNotification -> TriggerClientEvent('QBCore:Notify')

xPlayer.triggerEvent -> None (dont bother)

xPlayer.updateCoords -> None (dont bother)

esx:getSharedObject -> QBCore:GetObject

esx:setJob -> QBCore:Client:OnJobUpdate

esx:onPlayerSpawn -> QBCore:Client:OnPlayerLoaded

playerSpawned -> QBCore:Client:OnPlayerLoaded (spawnmanager compatibility)

esx:addInventoryItem -> QBCore:Server:AddItem

esx:removeInventoryItem -> QBCore:Server:RemoveItem

esx:useItem -> QBCore:Server:UseItem

MySQL.Async.fetchScalar() -> exports['ghmattimysql']:scalar() or QBCore.Functions.ExecuteSql(true,

MySQL.Async.fetchAll() -> exports['ghmattimysql']:execute() or QBCore.Functions.ExecuteSql(true,

MySQL.Async.execute() -> exports['ghmattimysql']:execute() or QBCore.Functions.ExecuteSql(false, 


    QBCore.Functions.GetPlayerData = function(cb)

    QBCore.Functions.GetPlayers = function()
    
    QBCore.Functions.DrawText = function(x, y, width, height, scale, r, g, b, a, text)
    
    QBCore.Functions.DrawText3D = function(x, y, z, text)
    
    QBCore.Functions.GetCoords = function(entity)
    
    QBCore.Functions.SpawnVehicle = function(model, cb, coords, isnetworked)
    
    QBCore.Functions.DeleteVehicle = function(vehicle)
    
    QBCore.Functions.Notify = function(text, textype, length)
    
    QBCore.Functions.TriggerCallback = function(name, cb, ...)
    
    QBCore.Functions.EnumerateEntities = function(initFunc, moveFunc, disposeFunc)
    
    QBCore.Functions.GetVehicles = function()
    
    QBCore.Functions.GetPeds = function(ignoreList)
    
    QBCore.Functions.GetClosestVehicle = function(coords)
    
    QBCore.Functions.GetClosestPed = function(coords, ignoreList)
    
    QBCore.Functions.GetClosestPlayer = function(coords)
    
    QBCore.Functions.GetPlayersFromCoords = function(coords, distance)
    
    QBCore.Functions.HasItem = function(source, cb, item)
    
    QBCore.Functions.Progressbar = function(name, label, duration, useWhileDead, canCancel, disableControls, animation, prop, propTwo, onFinish, onCancel)
    
    QBCore.Functions.GetVehicleProperties = function(vehicle)
    
    QBCore.Functions.SetVehicleProperties = function(vehicle, props) 

    QBCore.Functions.ExecuteSql = function(wait, query, cb) 

    QBCore.Functions.GetIdentifier = function(source, idtype) 
            
    QBCore.Functions.GetSource = function(identifier)
            
    QBCore.Functions.GetPlayer = function(source)
            
    QBCore.Functions.GetPlayerByCitizenId = function(citizenid)
            
    QBCore.Functions.GetPlayerByPhone = function(number)
            
    QBCore.Functions.GetPlayers = function()
            
    QBCore.Functions.CreateCallback = function(name, cb)
            
    QBCore.Functions.TriggerCallback = function(name, source, cb, ...)
            
    QBCore.Functions.CreateUseableItem = function(item, cb)
            
    QBCore.Functions.CanUseItem = function(item)
            
    QBCore.Functions.UseItem = function(source, item)
            
    QBCore.Functions.AddPermission = function(source, permission)
            
    QBCore.Functions.RemovePermission = function(source)
            
    QBCore.Functions.HasPermission = function(source, permission)
            
    QBCore.Functions.GetPermission = function(source)
            
    QBCore.Functions.IsPlayerBanned = function (source) 

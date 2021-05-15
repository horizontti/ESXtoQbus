# ESXtoQbus
How to convert ESX to Qbus

ESX = nil

Citizen.CreateThread(function()                                         |     QBCore = nil 
  while ESX == nil do                                                   |
    TriggerEvent('esx:getSharedObject', function(obj) ESX = obj end)    |     Citizen.CreateThread(function()
    Citizen.Wait(amount)                                                |         while QBCore == nil do
  end                                                                   |           TriggerEvent('QBCore:GetObject', function(obj) QBCore = obj end)  
end)                                                                    |           Citizen.Wait(amount)
                                                                        |         end
                                                                        |     end)


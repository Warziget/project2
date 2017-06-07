       Original script from : Kyominii --> https://forum.fivem.net/t/release-cops-fivem-v1-2-0-06-05-2017/17460
       Modification by Warziget 

        ---------------------- You need to put it just below the "end)" of the "remove yellow jacket" ------
        ---------------------- You also need to add buttons in config.lua ----------------------------------
        
        elseif btn == txt[config.lang]["cloackroom_add_police_cap_title"] then
            Citizen.CreateThread(function()
                if(GetEntityModel(GetPlayerPed(-1)) == hashSkin) then
                    SetPedPropIndex(GetPlayerPed(-1), 0, 46, 0, 2) -- casquette de police
                else
                    SetPedPropIndex(GetPlayerPed(-1), 0, 46, 0, 2) -- casquette de police
                end
            end)
        elseif btn == txt[config.lang]["cloackroom_remove_police_cap_title"] then
            Citizen.CreateThread(function()
                ClearPedProp(GetPlayerPed(-1),0) -- Enlever les chapeaux
            end)
            
       ----------------- About adding a cap directly in "giveUniform" here is an exemple of my modification -----------
       ----------------- Directly in "giveUniform" or you personal fonction --------------------------------------------
       
       function giveUniforme()
    Citizen.CreateThread(function()
        if(config.enableOutfits == true) then
            if(GetEntityModel(GetPlayerPed(-1)) == hashSkin) then

                SetPedComponentVariation(GetPlayerPed(-1), 1, 0, 0, 0)    -- Enleve cagoule, masque etc... -- #Warziget
                SetPedPropIndex(GetPlayerPed(-1), 0, 46, 0, 2)            -- Casquette de police -- #Warziget
                SetPedComponentVariation(GetPlayerPed(-1), 3, 52, 0, 2)   -- Main non bugué -- #Warziget
                SetPedPropIndex(GetPlayerPed(-1), 1, 5, 0, 2)             -- Sunglasses
                SetPedPropIndex(GetPlayerPed(-1), 2, 0, 0, 2)             -- Bluetoothn earphone
                SetPedComponentVariation(GetPlayerPed(-1), 11, 55, 0, 2)  -- Shirt
                SetPedComponentVariation(GetPlayerPed(-1), 8, 58, 0, 2)   -- Nightstick decoration
                SetPedComponentVariation(GetPlayerPed(-1), 4, 35, 0, 2)   -- Pants
                SetPedComponentVariation(GetPlayerPed(-1), 6, 24, 0, 2)   -- Shooes
                SetPedComponentVariation(GetPlayerPed(-1), 10, 8, 0, 2)   -- Rank

            else
            
       ---------------- (I didn't post the end of the code but you know where it take place)----------------------------
       
       Original script from : Kyominii --> https://forum.fivem.net/t/release-cops-fivem-v1-2-0-06-05-2017/17460
       Modification by Warziget 

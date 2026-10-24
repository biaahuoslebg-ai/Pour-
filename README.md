-- Exemple d'un script nettoyé et allégé pour Delta
local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Vérification de sécurité pour éviter les doublons
if getgenv().Running then
    warn("Le script tourne déjà !")
    return
end
getgenv().Running = true

print("Script Steal a Brainrot lancé avec succès sur Delta !")

-- Boucle propre et légère
task.spawn(function()
    while getgenv().Running do
        pcall(function()
            -- Ton code de logique simplifié ici
            -- (ex: recherche de podiums et interaction directe)
        end)
        task.wait(1) -- Pose une petite pause pour ne pas faire lagger le jeu ou crasher l'exécuteur
    end
end)

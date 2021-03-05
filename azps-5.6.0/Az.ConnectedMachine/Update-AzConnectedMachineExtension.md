---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: e6da084f13d85f8c4f5a8934cd5fd4f05882c251
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012321"
---
# <span data-ttu-id="51df3-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="51df3-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="51df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51df3-102">SYNOPSIS</span></span>
<span data-ttu-id="51df3-103">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="51df3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51df3-104">SYNTAX</span></span>

### <span data-ttu-id="51df3-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="51df3-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="51df3-106">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="51df3-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51df3-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="51df3-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51df3-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="51df3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51df3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="51df3-109">DESCRIPTION</span></span>
<span data-ttu-id="51df3-110">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="51df3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51df3-111">EXAMPLES</span></span>

### <span data-ttu-id="51df3-112">Przykład 1. Aktualizowanie rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="51df3-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="51df3-113">Aktualizuje rozszerzenie na określonym komputerze.</span><span class="sxs-lookup"><span data-stu-id="51df3-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="51df3-114">Przykład 2. Aktualizowanie rozszerzenia za pomocą lokalizacji określonej za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="51df3-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="51df3-115">Aktualizuje określone rozszerzenie przekazywane za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="51df3-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="51df3-116">W tym miejscu używamy rozszerzenia przekazywanego za pośrednictwem potoku, aby pomóc nam w określeniu, na którym rozszerzeniu chcemy pracować, i określamy, co chcemy zmienić za pośrednictwem normalnych parametrów `-Settings` (np.)</span><span class="sxs-lookup"><span data-stu-id="51df3-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="51df3-117">Przykład 3. Aktualizowanie rozszerzenia przy użyciu parametrów rozszerzenia określonych za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="51df3-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="51df3-118">Aktualizuje określone rozszerzenie przekazywane za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="51df3-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="51df3-119">Tutaj używamy rozszerzenia przekazywanego za pośrednictwem potoku, aby udostępnić zmiany, które chcemy wprowadzić w ramach rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="51df3-120">Lokalizacja rozszerzenia nie jest pobierana za pośrednictwem potoku, lecz za pośrednictwem parametrów określonych normalnie (przez parametr splat).</span><span class="sxs-lookup"><span data-stu-id="51df3-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="51df3-121">Przykład 4. Używanie obiektu rozszerzenia jako lokalizacji i parametrów aktualizacji</span><span class="sxs-lookup"><span data-stu-id="51df3-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="51df3-122">Aktualizuje określone rozszerzenie przekazywane za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="51df3-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="51df3-123">W tym miejscu używamy rozszerzenia przekazywanego za pośrednictwem potoku, aby pomóc nam w identyfikować, nad którym rozszerzeniem chcemy pracować.</span><span class="sxs-lookup"><span data-stu-id="51df3-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="51df3-124">Oprócz tego do określenia, co należy zaktualizować, używamy parametrów obiektu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="51df3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51df3-125">PARAMETERS</span></span>

### <span data-ttu-id="51df3-126">— AsJob</span><span class="sxs-lookup"><span data-stu-id="51df3-126">-AsJob</span></span>
<span data-ttu-id="51df3-127">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="51df3-127">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="51df3-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="51df3-129">Wskazuje, czy rozszerzenie powinno używać nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="51df3-130">Jednak po wdrożeniu rozszerzenie nie będzie uaktualniać wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="51df3-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51df3-131">-DefaultProfile</span></span>
<span data-ttu-id="51df3-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51df3-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-133">-ExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="51df3-133">-ExtensionParameter</span></span>
<span data-ttu-id="51df3-134">W tym artykule opisano aktualizację rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="51df3-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="51df3-135">Aby skonstruować, zobacz sekcję UWAGI, aby uzyskać informacje o właściwościach właściwości EXTENSIONPARAMETERS i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="51df3-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="51df3-136">-ForceRerun</span></span>
<span data-ttu-id="51df3-137">Jak należy wymusić aktualizację programu obsługi rozszerzenia, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="51df3-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51df3-138">-InputObject</span></span>
<span data-ttu-id="51df3-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="51df3-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-140">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="51df3-140">-MachineName</span></span>
<span data-ttu-id="51df3-141">Nazwa komputera, na którym należy utworzyć lub zaktualizować rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="51df3-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-142">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="51df3-142">-Name</span></span>
<span data-ttu-id="51df3-143">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="51df3-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="51df3-144">-NoWait</span></span>
<span data-ttu-id="51df3-145">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="51df3-145">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="51df3-146">-ProtectedSetting</span></span>
<span data-ttu-id="51df3-147">Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault albo nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="51df3-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-148">— Publisher</span><span class="sxs-lookup"><span data-stu-id="51df3-148">-Publisher</span></span>
<span data-ttu-id="51df3-149">Nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51df3-150">-ResourceGroupName</span></span>
<span data-ttu-id="51df3-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51df3-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-152">— Ustawienie</span><span class="sxs-lookup"><span data-stu-id="51df3-152">-Setting</span></span>
<span data-ttu-id="51df3-153">Formatowane ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-154">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51df3-154">-SubscriptionId</span></span>
<span data-ttu-id="51df3-155">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="51df3-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="51df3-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="51df3-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-157">— Tag</span><span class="sxs-lookup"><span data-stu-id="51df3-157">-Tag</span></span>
<span data-ttu-id="51df3-158">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="51df3-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-159">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="51df3-159">-Type</span></span>
<span data-ttu-id="51df3-160">Określa typ rozszerzenia. Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="51df3-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="51df3-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="51df3-162">Określa wersję programu obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="51df3-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51df3-163">-Confirm</span></span>
<span data-ttu-id="51df3-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51df3-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51df3-165">-WhatIf</span></span>
<span data-ttu-id="51df3-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51df3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51df3-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51df3-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51df3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51df3-168">CommonParameters</span></span>
<span data-ttu-id="51df3-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51df3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51df3-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51df3-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51df3-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51df3-171">INPUTS</span></span>

### <span data-ttu-id="51df3-172">Microsoft.Azure.PowerShell.Cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="51df3-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="51df3-173">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="51df3-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="51df3-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51df3-174">OUTPUTS</span></span>

### <span data-ttu-id="51df3-175">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="51df3-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="51df3-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51df3-176">NOTES</span></span>

<span data-ttu-id="51df3-177">ALIASY</span><span class="sxs-lookup"><span data-stu-id="51df3-177">ALIASES</span></span>

<span data-ttu-id="51df3-178">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51df3-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51df3-179">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="51df3-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51df3-180">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51df3-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51df3-181">EXTENSIONPARAMETERS: <IMachineExtensionUpdate> W tym artykule opisano aktualizację rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="51df3-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="51df3-182">`[Tag <IUpdateResourceTags>]`: tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="51df3-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="51df3-183">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="51df3-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="51df3-184">`[AutoUpgradeMinorVersion <Boolean?>]`: wskazuje, czy rozszerzenie powinno korzystać z nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="51df3-185">Jednak po wdrożeniu rozszerzenie nie będzie uaktualniać wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="51df3-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="51df3-186">`[ForceUpdateTag <String>]`: Jak należy wymusić aktualizację programu obsługi rozszerzeń, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="51df3-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="51df3-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault lub nie może mieć żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="51df3-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="51df3-188">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="51df3-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="51df3-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Sformatowane ustawienia publiczne rozszerzenia w formacie Json.</span><span class="sxs-lookup"><span data-stu-id="51df3-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="51df3-190">`[Type <String>]`: określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="51df3-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="51df3-191">`[TypeHandlerVersion <String>]`: określa wersję programu obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="51df3-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="51df3-192">INPUTOBJECT: <IConnectedMachineIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="51df3-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51df3-193">`[ExtensionName <String>]`: nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="51df3-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="51df3-194">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="51df3-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51df3-195">`[Name <String>]`: nazwa komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="51df3-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="51df3-196">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51df3-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="51df3-197">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="51df3-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="51df3-198">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="51df3-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="51df3-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51df3-199">RELATED LINKS</span></span>


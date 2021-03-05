---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: accea82dd6594d71f627d6c3e32943d004fa35e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012346"
---
# <span data-ttu-id="44e69-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="44e69-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="44e69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44e69-102">SYNOPSIS</span></span>
<span data-ttu-id="44e69-103">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="44e69-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="44e69-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44e69-104">SYNTAX</span></span>

### <span data-ttu-id="44e69-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="44e69-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="44e69-106">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="44e69-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44e69-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="44e69-107">DESCRIPTION</span></span>
<span data-ttu-id="44e69-108">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="44e69-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="44e69-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44e69-109">EXAMPLES</span></span>

### <span data-ttu-id="44e69-110">Przykład 1. Ustawianie rozszerzenia na komputerze</span><span class="sxs-lookup"><span data-stu-id="44e69-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="44e69-111">Ustawia rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="44e69-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="44e69-112">Przykład 2. Ustawianie rozszerzenia z parametrami rozszerzenia określonymi za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="44e69-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="44e69-113">To ustawienie rozszerzenia z parametrami rozszerzenia dostarczonymi przez obiekt przekazany za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="44e69-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="44e69-114">To doskonałe, jeśli chcesz chwycić parametry jednego komputera i zastosować je do innego komputera.</span><span class="sxs-lookup"><span data-stu-id="44e69-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="44e69-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44e69-115">PARAMETERS</span></span>

### <span data-ttu-id="44e69-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="44e69-116">-AsJob</span></span>
<span data-ttu-id="44e69-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="44e69-117">Run the command as a job</span></span>

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

### <span data-ttu-id="44e69-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="44e69-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="44e69-119">Wskazuje, czy rozszerzenie powinno używać nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="44e69-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="44e69-120">Jednak po wdrożeniu rozszerzenie nie będzie uaktualniać wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="44e69-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e69-121">-DefaultProfile</span></span>
<span data-ttu-id="44e69-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44e69-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44e69-123">-ExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="44e69-123">-ExtensionParameter</span></span>
<span data-ttu-id="44e69-124">W tym artykule opisano rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="44e69-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="44e69-125">Aby skonstruować, zobacz sekcję UWAGI, aby uzyskać informacje o właściwościach właściwości EXTENSIONPARAMETERS i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="44e69-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="44e69-126">-ExtensionType</span></span>
<span data-ttu-id="44e69-127">Określa typ rozszerzenia. Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="44e69-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="44e69-128">-ForceRerun</span></span>
<span data-ttu-id="44e69-129">Jak należy wymusić aktualizację programu obsługi rozszerzenia, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="44e69-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="44e69-130">-Location</span></span>
<span data-ttu-id="44e69-131">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="44e69-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-132">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="44e69-132">-MachineName</span></span>
<span data-ttu-id="44e69-133">Nazwa komputera, na którym należy utworzyć lub zaktualizować rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="44e69-133">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="44e69-134">-Name</span></span>
<span data-ttu-id="44e69-135">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="44e69-135">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="44e69-136">-NoWait</span></span>
<span data-ttu-id="44e69-137">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="44e69-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44e69-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="44e69-138">-ProtectedSetting</span></span>
<span data-ttu-id="44e69-139">Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault albo nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="44e69-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-140">— Publisher</span><span class="sxs-lookup"><span data-stu-id="44e69-140">-Publisher</span></span>
<span data-ttu-id="44e69-141">Nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="44e69-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e69-142">-ResourceGroupName</span></span>
<span data-ttu-id="44e69-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="44e69-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-144">— Ustawienie</span><span class="sxs-lookup"><span data-stu-id="44e69-144">-Setting</span></span>
<span data-ttu-id="44e69-145">Formatowane ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="44e69-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-146">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44e69-146">-SubscriptionId</span></span>
<span data-ttu-id="44e69-147">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44e69-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="44e69-148">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="44e69-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-149">— Tag</span><span class="sxs-lookup"><span data-stu-id="44e69-149">-Tag</span></span>
<span data-ttu-id="44e69-150">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="44e69-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="44e69-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="44e69-152">Określa wersję programu obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="44e69-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e69-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44e69-153">-Confirm</span></span>
<span data-ttu-id="44e69-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44e69-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44e69-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44e69-155">-WhatIf</span></span>
<span data-ttu-id="44e69-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44e69-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44e69-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="44e69-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44e69-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e69-158">CommonParameters</span></span>
<span data-ttu-id="44e69-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44e69-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e69-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44e69-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e69-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44e69-161">INPUTS</span></span>

### <span data-ttu-id="44e69-162">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="44e69-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="44e69-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44e69-163">OUTPUTS</span></span>

### <span data-ttu-id="44e69-164">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="44e69-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="44e69-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44e69-165">NOTES</span></span>

<span data-ttu-id="44e69-166">ALIASY</span><span class="sxs-lookup"><span data-stu-id="44e69-166">ALIASES</span></span>

<span data-ttu-id="44e69-167">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44e69-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44e69-168">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="44e69-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44e69-169">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44e69-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44e69-170">EXTENSIONPARAMETERS: <IMachineExtension> W tym artykule opisano rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="44e69-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="44e69-171">`Location <String>`: lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="44e69-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="44e69-172">`[Tag <ITrackedResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="44e69-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="44e69-173">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="44e69-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="44e69-174">`[AutoUpgradeMinorVersion <Boolean?>]`: wskazuje, czy rozszerzenie powinno korzystać z nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="44e69-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="44e69-175">Jednak po wdrożeniu rozszerzenie nie będzie uaktualniać wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="44e69-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="44e69-176">`[ForceUpdateTag <String>]`: Jak należy wymusić aktualizację programu obsługi rozszerzeń, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="44e69-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="44e69-177">`[MachineExtensionType <String>]`: określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="44e69-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="44e69-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault lub nie może mieć żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="44e69-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="44e69-179">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="44e69-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="44e69-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Sformatowane ustawienia publiczne rozszerzenia w formacie Json.</span><span class="sxs-lookup"><span data-stu-id="44e69-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="44e69-181">`[TypeHandlerVersion <String>]`: określa wersję programu obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="44e69-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="44e69-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44e69-182">RELATED LINKS</span></span>


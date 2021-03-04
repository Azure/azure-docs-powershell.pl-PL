---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: df2e1de102143f227178b45ea14264f9e61d86a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012394"
---
# <span data-ttu-id="5d5fe-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d5fe-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="5d5fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5fe-103">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="5d5fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d5fe-104">SYNTAX</span></span>

### <span data-ttu-id="5d5fe-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="5d5fe-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d5fe-106">Tworzenie</span><span class="sxs-lookup"><span data-stu-id="5d5fe-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d5fe-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d5fe-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5d5fe-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5d5fe-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d5fe-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d5fe-109">DESCRIPTION</span></span>
<span data-ttu-id="5d5fe-110">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="5d5fe-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d5fe-111">EXAMPLES</span></span>

### <span data-ttu-id="5d5fe-112">Przykład 1. Dodawanie nowego rozszerzenia na komputerze</span><span class="sxs-lookup"><span data-stu-id="5d5fe-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="5d5fe-113">Ustawia rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="5d5fe-114">Przykład 2. Dodawanie nowego rozszerzenia z parametrami rozszerzenia określonymi za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="5d5fe-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="5d5fe-115">Powoduje to utworzenie nowego rozszerzenia z parametrami rozszerzenia dostarczonymi przez obiekt przekazany za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="5d5fe-116">To doskonałe, jeśli chcesz chwycić parametry jednego komputera i zastosować je do innego komputera.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="5d5fe-117">Przykład 3. Dodawanie nowego rozszerzenia z lokalizacją określoną za pośrednictwem potoku</span><span class="sxs-lookup"><span data-stu-id="5d5fe-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="5d5fe-118">Powoduje to utworzenie nowego rozszerzenia komputera przy użyciu tożsamości udostępnianej za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="5d5fe-119">Prawdopodobnie tego nie zrobisz, ale jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="5d5fe-120">Przykład 4. Dodawanie nowego rozszerzenia przy użyciu obiektu rozszerzenia jako lokalizacji i parametrów aktualizacji</span><span class="sxs-lookup"><span data-stu-id="5d5fe-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="5d5fe-121">Powoduje to utworzenie nowego rozszerzenia komputera przy użyciu tożsamości udostępnianej za pośrednictwem potoku i szczegółów rozszerzenia dostarczonych przez obiekt rozszerzenia przekazany.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="5d5fe-122">Prawdopodobnie tego nie zrobisz, ale jest to możliwe.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="5d5fe-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d5fe-123">PARAMETERS</span></span>

### <span data-ttu-id="5d5fe-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5d5fe-124">-AsJob</span></span>
<span data-ttu-id="5d5fe-125">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="5d5fe-125">Run the command as a job</span></span>

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

### <span data-ttu-id="5d5fe-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5d5fe-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5d5fe-127">Wskazuje, czy rozszerzenie powinno używać nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="5d5fe-128">Jednak po wdrożeniu rozszerzenie nie będzie uaktualniać wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5fe-129">-DefaultProfile</span></span>
<span data-ttu-id="5d5fe-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d5fe-131">-ExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="5d5fe-131">-ExtensionParameter</span></span>
<span data-ttu-id="5d5fe-132">W tym artykule opisano rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="5d5fe-133">Aby skonstruować, zobacz sekcję UWAGI, aby uzyskać informacje o właściwościach właściwości EXTENSIONPARAMETERS i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="5d5fe-134">-ExtensionType</span></span>
<span data-ttu-id="5d5fe-135">Określa typ rozszerzenia. Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="5d5fe-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5d5fe-136">-ForceRerun</span></span>
<span data-ttu-id="5d5fe-137">Jak należy wymusić aktualizację programu obsługi rozszerzenia, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d5fe-138">-InputObject</span></span>
<span data-ttu-id="5d5fe-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5d5fe-140">-Location</span></span>
<span data-ttu-id="5d5fe-141">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="5d5fe-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-142">— Nazwa_komputera</span><span class="sxs-lookup"><span data-stu-id="5d5fe-142">-MachineName</span></span>
<span data-ttu-id="5d5fe-143">Nazwa komputera, na którym należy utworzyć lub zaktualizować rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-144">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5d5fe-144">-Name</span></span>
<span data-ttu-id="5d5fe-145">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5d5fe-146">-NoWait</span></span>
<span data-ttu-id="5d5fe-147">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="5d5fe-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d5fe-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="5d5fe-148">-ProtectedSetting</span></span>
<span data-ttu-id="5d5fe-149">Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault albo nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-150">— Publisher</span><span class="sxs-lookup"><span data-stu-id="5d5fe-150">-Publisher</span></span>
<span data-ttu-id="5d5fe-151">Nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5fe-152">-ResourceGroupName</span></span>
<span data-ttu-id="5d5fe-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-154">— Ustawienie</span><span class="sxs-lookup"><span data-stu-id="5d5fe-154">-Setting</span></span>
<span data-ttu-id="5d5fe-155">Formatowane ustawienia publiczne rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-156">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d5fe-156">-SubscriptionId</span></span>
<span data-ttu-id="5d5fe-157">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d5fe-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-159">— Tag</span><span class="sxs-lookup"><span data-stu-id="5d5fe-159">-Tag</span></span>
<span data-ttu-id="5d5fe-160">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5d5fe-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="5d5fe-162">Określa wersję programu obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5fe-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d5fe-163">-Confirm</span></span>
<span data-ttu-id="5d5fe-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5fe-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5fe-165">-WhatIf</span></span>
<span data-ttu-id="5d5fe-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d5fe-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5fe-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5fe-168">CommonParameters</span></span>
<span data-ttu-id="5d5fe-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5fe-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d5fe-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5fe-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d5fe-171">INPUTS</span></span>

### <span data-ttu-id="5d5fe-172">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d5fe-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="5d5fe-173">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="5d5fe-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="5d5fe-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d5fe-174">OUTPUTS</span></span>

### <span data-ttu-id="5d5fe-175">Microsoft.Azure.PowerShell.cmdlet.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5d5fe-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="5d5fe-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d5fe-176">NOTES</span></span>

<span data-ttu-id="5d5fe-177">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5d5fe-177">ALIASES</span></span>

<span data-ttu-id="5d5fe-178">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d5fe-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d5fe-179">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d5fe-180">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d5fe-181">EXTENSIONPARAMETERS: <IMachineExtension> W tym artykule opisano rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="5d5fe-182">`Location <String>`: lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="5d5fe-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="5d5fe-183">`[Tag <ITrackedResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="5d5fe-184">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5d5fe-185">`[AutoUpgradeMinorVersion <Boolean?>]`: wskazuje, czy rozszerzenie powinno korzystać z nowszej wersji pomocniczej, jeśli jest dostępne w momencie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="5d5fe-186">Jednak po wdrożeniu rozszerzenie nie będzie uaktualniać wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="5d5fe-187">`[ForceUpdateTag <String>]`: Jak należy wymusić aktualizację programu obsługi rozszerzeń, nawet jeśli konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="5d5fe-188">`[MachineExtensionType <String>]`: określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="5d5fe-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="5d5fe-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Rozszerzenie może zawierać ustawienia protectedSettings lub protectedSettingsFromKeyVault lub nie może mieć żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="5d5fe-190">`[Publisher <String>]`: nazwa wydawcy programu obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="5d5fe-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Sformatowane ustawienia publiczne rozszerzenia w formacie Json.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="5d5fe-192">`[TypeHandlerVersion <String>]`: określa wersję programu obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="5d5fe-193">INPUTOBJECT: <IConnectedMachineIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="5d5fe-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d5fe-194">`[ExtensionName <String>]`: nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="5d5fe-195">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5d5fe-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d5fe-196">`[Name <String>]`: nazwa komputera hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="5d5fe-197">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5d5fe-198">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d5fe-199">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="5d5fe-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5d5fe-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d5fe-200">RELATED LINKS</span></span>


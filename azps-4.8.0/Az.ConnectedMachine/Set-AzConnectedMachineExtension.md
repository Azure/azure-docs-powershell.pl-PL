---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063565"
---
# <span data-ttu-id="60095-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="60095-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="60095-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60095-102">SYNOPSIS</span></span>
<span data-ttu-id="60095-103">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="60095-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="60095-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60095-104">SYNTAX</span></span>

### <span data-ttu-id="60095-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60095-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="60095-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="60095-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60095-107">Opis</span><span class="sxs-lookup"><span data-stu-id="60095-107">DESCRIPTION</span></span>
<span data-ttu-id="60095-108">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="60095-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="60095-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60095-109">EXAMPLES</span></span>

### <span data-ttu-id="60095-110">Przykład 1: Ustawianie rozszerzenia na komputerze</span><span class="sxs-lookup"><span data-stu-id="60095-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="60095-111">Ustawia rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="60095-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="60095-112">Przykład 2: Ustawianie rozszerzenia z parametrami rozszerzenia określonymi za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="60095-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="60095-113">Spowoduje to ustawienie rozszerzenia z parametrami rozszerzenia dostarczonymi przez obiekt przekazany za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="60095-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="60095-114">Jest to przydatne, jeśli chcesz poszukać parametrów jednego komputera i zastosować go do innego komputera.</span><span class="sxs-lookup"><span data-stu-id="60095-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="60095-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60095-115">PARAMETERS</span></span>

### <span data-ttu-id="60095-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60095-116">-AsJob</span></span>
<span data-ttu-id="60095-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="60095-117">Run the command as a job</span></span>

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

### <span data-ttu-id="60095-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="60095-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="60095-119">Wskazuje, czy rozszerzenie ma używać nowszej wersji pomocniczej, jeśli jest dostępna w czasie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="60095-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="60095-120">Po wdrożeniu rozszerzenie nie będzie jednak uaktualnić wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="60095-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="60095-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60095-121">-DefaultProfile</span></span>
<span data-ttu-id="60095-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60095-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60095-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="60095-123">-ExtensionParameter</span></span>
<span data-ttu-id="60095-124">W tym artykule opisano rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="60095-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="60095-125">Aby skonstruować, zobacz sekcję notatki dla właściwości EXTENSIONPARAMETER i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="60095-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="60095-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="60095-126">-ExtensionType</span></span>
<span data-ttu-id="60095-127">Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="60095-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="60095-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="60095-128">-ForceRerun</span></span>
<span data-ttu-id="60095-129">W jaki sposób program obsługi rozszerzeń powinien być zmuszony do aktualizacji, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="60095-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="60095-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="60095-130">-Location</span></span>
<span data-ttu-id="60095-131">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="60095-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="60095-132">-NazwaKomputera</span><span class="sxs-lookup"><span data-stu-id="60095-132">-MachineName</span></span>
<span data-ttu-id="60095-133">Nazwa komputera, na którym ma zostać utworzone lub zaktualizowane rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="60095-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="60095-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60095-134">-Name</span></span>
<span data-ttu-id="60095-135">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="60095-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="60095-136">-Nowait</span><span class="sxs-lookup"><span data-stu-id="60095-136">-NoWait</span></span>
<span data-ttu-id="60095-137">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="60095-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="60095-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="60095-138">-ProtectedSetting</span></span>
<span data-ttu-id="60095-139">Rozszerzenie może zawierać protectedSettings lub protectedSettingsFromKeyVault lub nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="60095-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="60095-140">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="60095-140">-Publisher</span></span>
<span data-ttu-id="60095-141">Nazwa wydawcy obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="60095-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="60095-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60095-142">-ResourceGroupName</span></span>
<span data-ttu-id="60095-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60095-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="60095-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="60095-144">-Setting</span></span>
<span data-ttu-id="60095-145">Ustawienia publiczne w formacie JSON dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="60095-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="60095-146">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="60095-146">-SubscriptionId</span></span>
<span data-ttu-id="60095-147">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="60095-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60095-148">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="60095-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="60095-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="60095-149">-Tag</span></span>
<span data-ttu-id="60095-150">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="60095-150">Resource tags.</span></span>

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

### <span data-ttu-id="60095-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="60095-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="60095-152">Określa wersję obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="60095-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="60095-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60095-153">-Confirm</span></span>
<span data-ttu-id="60095-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60095-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60095-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60095-155">-WhatIf</span></span>
<span data-ttu-id="60095-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60095-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60095-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60095-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60095-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60095-158">CommonParameters</span></span>
<span data-ttu-id="60095-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60095-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60095-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60095-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60095-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60095-161">INPUTS</span></span>

### <span data-ttu-id="60095-162">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="60095-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="60095-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60095-163">OUTPUTS</span></span>

### <span data-ttu-id="60095-164">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="60095-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="60095-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60095-165">NOTES</span></span>

<span data-ttu-id="60095-166">PISUJE</span><span class="sxs-lookup"><span data-stu-id="60095-166">ALIASES</span></span>

<span data-ttu-id="60095-167">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60095-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60095-168">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="60095-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60095-169">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60095-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60095-170">EXTENSIONPARAMETER <IMachineExtension> : Opisuje rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="60095-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="60095-171">`Location <String>`: Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="60095-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="60095-172">`[Tag <ITrackedResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="60095-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="60095-173">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="60095-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="60095-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Wskazuje, czy rozszerzenie ma używać nowszej wersji pomocniczej, jeśli jest dostępna w czasie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="60095-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="60095-175">Po wdrożeniu rozszerzenie nie będzie jednak uaktualnić wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="60095-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="60095-176">`[ForceUpdateTag <String>]`: Jak należy wymusić aktualizację procedury obsługi rozszerzeń, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="60095-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="60095-177">`[MachineExtensionType <String>]`: Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="60095-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="60095-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Rozszerzenie może zawierać co najmniej protectedSettings lub protectedSettingsFromKeyVault lub bez ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="60095-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="60095-179">`[Publisher <String>]`: Nazwa wydawcy obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="60095-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="60095-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Ustawienia publiczne w formacie JSON dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="60095-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="60095-181">`[TypeHandlerVersion <String>]`: Określa wersję obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="60095-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="60095-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60095-182">RELATED LINKS</span></span>


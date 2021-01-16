---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325645"
---
# <span data-ttu-id="216ae-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="216ae-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="216ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="216ae-102">SYNOPSIS</span></span>
<span data-ttu-id="216ae-103">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="216ae-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="216ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="216ae-104">SYNTAX</span></span>

### <span data-ttu-id="216ae-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="216ae-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="216ae-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="216ae-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="216ae-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="216ae-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="216ae-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="216ae-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="216ae-109">Opis</span><span class="sxs-lookup"><span data-stu-id="216ae-109">DESCRIPTION</span></span>
<span data-ttu-id="216ae-110">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="216ae-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="216ae-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="216ae-111">EXAMPLES</span></span>

### <span data-ttu-id="216ae-112">Przykład 1: Dodawanie nowego rozszerzenia do komputera</span><span class="sxs-lookup"><span data-stu-id="216ae-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="216ae-113">Ustawia rozszerzenie na komputerze.</span><span class="sxs-lookup"><span data-stu-id="216ae-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="216ae-114">Przykład 2: Dodawanie nowego rozszerzenia z parametrami rozszerzenia określonymi za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="216ae-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="216ae-115">Spowoduje to utworzenie nowego rozszerzenia z parametrami rozszerzenia dostarczonymi przez obiekt przekazany za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="216ae-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="216ae-116">Jest to przydatne, jeśli chcesz poszukać parametrów jednego komputera i zastosować go do innego komputera.</span><span class="sxs-lookup"><span data-stu-id="216ae-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="216ae-117">Przykład 3: Dodawanie nowego rozszerzenia z lokalizacją określoną za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="216ae-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="216ae-118">Spowoduje to utworzenie nowego rozszerzenia komputera przy użyciu tożsamości podanej za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="216ae-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="216ae-119">Prawdopodobnie nie będzie to możliwe.</span><span class="sxs-lookup"><span data-stu-id="216ae-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="216ae-120">Przykład 4: Dodawanie nowego rozszerzenia za pomocą obiektu rozszerzenia jako lokalizacji i parametrów do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="216ae-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="216ae-121">Spowoduje to utworzenie nowego rozszerzenia komputera przy użyciu tożsamości podanej za pośrednictwem rurociągu oraz informacji o rozszerzeniu dostarczonych przez obiekt przekazanego rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="216ae-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="216ae-122">Prawdopodobnie nie będzie to możliwe.</span><span class="sxs-lookup"><span data-stu-id="216ae-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="216ae-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="216ae-123">PARAMETERS</span></span>

### <span data-ttu-id="216ae-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="216ae-124">-AsJob</span></span>
<span data-ttu-id="216ae-125">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="216ae-125">Run the command as a job</span></span>

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

### <span data-ttu-id="216ae-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="216ae-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="216ae-127">Wskazuje, czy rozszerzenie ma używać nowszej wersji pomocniczej, jeśli jest dostępna w czasie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="216ae-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="216ae-128">Po wdrożeniu rozszerzenie nie będzie jednak uaktualnić wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="216ae-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="216ae-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216ae-129">-DefaultProfile</span></span>
<span data-ttu-id="216ae-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="216ae-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="216ae-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="216ae-131">-ExtensionParameter</span></span>
<span data-ttu-id="216ae-132">W tym artykule opisano rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="216ae-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="216ae-133">Aby skonstruować, zobacz sekcję notatki dla właściwości EXTENSIONPARAMETER i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="216ae-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="216ae-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="216ae-134">-ExtensionType</span></span>
<span data-ttu-id="216ae-135">Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="216ae-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="216ae-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="216ae-136">-ForceRerun</span></span>
<span data-ttu-id="216ae-137">W jaki sposób program obsługi rozszerzeń powinien być zmuszony do aktualizacji, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="216ae-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="216ae-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="216ae-138">-InputObject</span></span>
<span data-ttu-id="216ae-139">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="216ae-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="216ae-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="216ae-140">-Location</span></span>
<span data-ttu-id="216ae-141">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="216ae-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="216ae-142">-NazwaKomputera</span><span class="sxs-lookup"><span data-stu-id="216ae-142">-MachineName</span></span>
<span data-ttu-id="216ae-143">Nazwa komputera, na którym ma zostać utworzone lub zaktualizowane rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="216ae-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="216ae-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="216ae-144">-Name</span></span>
<span data-ttu-id="216ae-145">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="216ae-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="216ae-146">-Nowait</span><span class="sxs-lookup"><span data-stu-id="216ae-146">-NoWait</span></span>
<span data-ttu-id="216ae-147">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="216ae-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="216ae-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="216ae-148">-ProtectedSetting</span></span>
<span data-ttu-id="216ae-149">Rozszerzenie może zawierać protectedSettings lub protectedSettingsFromKeyVault lub nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="216ae-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="216ae-150">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="216ae-150">-Publisher</span></span>
<span data-ttu-id="216ae-151">Nazwa wydawcy obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="216ae-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="216ae-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="216ae-152">-ResourceGroupName</span></span>
<span data-ttu-id="216ae-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="216ae-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="216ae-154">-Setting</span><span class="sxs-lookup"><span data-stu-id="216ae-154">-Setting</span></span>
<span data-ttu-id="216ae-155">Ustawienia publiczne w formacie JSON dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="216ae-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="216ae-156">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="216ae-156">-SubscriptionId</span></span>
<span data-ttu-id="216ae-157">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="216ae-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="216ae-158">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="216ae-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="216ae-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="216ae-159">-Tag</span></span>
<span data-ttu-id="216ae-160">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="216ae-160">Resource tags.</span></span>

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

### <span data-ttu-id="216ae-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="216ae-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="216ae-162">Określa wersję obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="216ae-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="216ae-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="216ae-163">-Confirm</span></span>
<span data-ttu-id="216ae-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="216ae-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="216ae-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="216ae-165">-WhatIf</span></span>
<span data-ttu-id="216ae-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="216ae-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="216ae-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="216ae-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="216ae-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216ae-168">CommonParameters</span></span>
<span data-ttu-id="216ae-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="216ae-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216ae-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="216ae-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216ae-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="216ae-171">INPUTS</span></span>

### <span data-ttu-id="216ae-172">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="216ae-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="216ae-173">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="216ae-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="216ae-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="216ae-174">OUTPUTS</span></span>

### <span data-ttu-id="216ae-175">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="216ae-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="216ae-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="216ae-176">NOTES</span></span>

<span data-ttu-id="216ae-177">PISUJE</span><span class="sxs-lookup"><span data-stu-id="216ae-177">ALIASES</span></span>

<span data-ttu-id="216ae-178">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="216ae-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="216ae-179">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="216ae-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="216ae-180">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="216ae-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="216ae-181">EXTENSIONPARAMETER <IMachineExtension> : Opisuje rozszerzenie komputera.</span><span class="sxs-lookup"><span data-stu-id="216ae-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="216ae-182">`Location <String>`: Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="216ae-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="216ae-183">`[Tag <ITrackedResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="216ae-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="216ae-184">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="216ae-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="216ae-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Wskazuje, czy rozszerzenie ma używać nowszej wersji pomocniczej, jeśli jest dostępna w czasie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="216ae-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="216ae-186">Po wdrożeniu rozszerzenie nie będzie jednak uaktualnić wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="216ae-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="216ae-187">`[ForceUpdateTag <String>]`: Jak należy wymusić aktualizację procedury obsługi rozszerzeń, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="216ae-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="216ae-188">`[MachineExtensionType <String>]`: Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="216ae-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="216ae-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Rozszerzenie może zawierać co najmniej protectedSettings lub protectedSettingsFromKeyVault lub bez ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="216ae-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="216ae-190">`[Publisher <String>]`: Nazwa wydawcy obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="216ae-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="216ae-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Ustawienia publiczne w formacie JSON dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="216ae-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="216ae-192">`[TypeHandlerVersion <String>]`: Określa wersję obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="216ae-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="216ae-193">INPUTobject <IConnectedMachineIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="216ae-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="216ae-194">`[ExtensionName <String>]`: Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="216ae-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="216ae-195">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="216ae-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="216ae-196">`[Name <String>]`: Nazwa maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="216ae-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="216ae-197">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="216ae-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="216ae-198">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="216ae-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="216ae-199">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="216ae-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="216ae-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="216ae-200">RELATED LINKS</span></span>


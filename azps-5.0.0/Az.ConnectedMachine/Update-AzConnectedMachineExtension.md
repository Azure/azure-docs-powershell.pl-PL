---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233198"
---
# <span data-ttu-id="bdcb6-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bdcb6-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="bdcb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdcb6-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcb6-103">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="bdcb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdcb6-104">SYNTAX</span></span>

### <span data-ttu-id="bdcb6-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdcb6-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bdcb6-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="bdcb6-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bdcb6-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bdcb6-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bdcb6-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bdcb6-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bdcb6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bdcb6-109">DESCRIPTION</span></span>
<span data-ttu-id="bdcb6-110">Operacja tworzenia lub aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="bdcb6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdcb6-111">EXAMPLES</span></span>

### <span data-ttu-id="bdcb6-112">Przykład 1: aktualizowanie rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="bdcb6-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="bdcb6-113">Umożliwia zaktualizowanie rozszerzenia na określonym komputerze.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="bdcb6-114">Przykład 2: aktualizowanie rozszerzenia z lokalizacją określoną za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="bdcb6-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="bdcb6-115">Umożliwia zaktualizowanie określonego rozszerzenia przekazanego za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="bdcb6-116">W tym przypadku korzystamy z rozszerzenia przekazanego za pośrednictwem rurociągu, aby ułatwić nam zidentyfikowanie odpowiedniego rozszerzenia i określenie tego, co chcemy zmienić, przy użyciu zwykłych parametrów (takich jak `-Settings` ).</span><span class="sxs-lookup"><span data-stu-id="bdcb6-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="bdcb6-117">Przykład 3: aktualizowanie rozszerzenia przy użyciu parametrów rozszerzenia określonych za pośrednictwem rurociągu</span><span class="sxs-lookup"><span data-stu-id="bdcb6-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="bdcb6-118">Umożliwia zaktualizowanie określonego rozszerzenia przekazanego za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="bdcb6-119">W tym miejscu użyto rozszerzenia przekazanego za pośrednictwem rurociągu w celu wprowadzenia zmian, które chcemy wprowadzić na rozszerzeniu.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="bdcb6-120">Lokalizacja rozszerzenia nie jest pobierana za pośrednictwem rurociągu, ale zamiast parametrów określonych normalnie (za pomocą parametru Splat).</span><span class="sxs-lookup"><span data-stu-id="bdcb6-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="bdcb6-121">Przykład 4: Używanie obiektu rozszerzenia jako lokalizacji i parametrów do aktualizowania</span><span class="sxs-lookup"><span data-stu-id="bdcb6-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="bdcb6-122">Umożliwia zaktualizowanie określonego rozszerzenia przekazanego za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="bdcb6-123">W tym przypadku korzystamy z rozszerzenia przekazanego za pośrednictwem potoku, aby ułatwić nam zidentyfikowanie rozszerzenia, na którym chcemy pracować.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="bdcb6-124">Oprócz tego, używamy parametrów obiektu rozszerzeń, aby określić, co należy zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="bdcb6-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdcb6-125">PARAMETERS</span></span>

### <span data-ttu-id="bdcb6-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdcb6-126">-AsJob</span></span>
<span data-ttu-id="bdcb6-127">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="bdcb6-127">Run the command as a job</span></span>

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

### <span data-ttu-id="bdcb6-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bdcb6-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bdcb6-129">Wskazuje, czy rozszerzenie ma używać nowszej wersji pomocniczej, jeśli jest dostępna w czasie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="bdcb6-130">Po wdrożeniu rozszerzenie nie będzie jednak uaktualnić wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="bdcb6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcb6-131">-DefaultProfile</span></span>
<span data-ttu-id="bdcb6-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdcb6-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="bdcb6-133">-ExtensionParameter</span></span>
<span data-ttu-id="bdcb6-134">W tym artykule opisano aktualizację rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="bdcb6-135">Aby skonstruować, zobacz sekcję notatki dla właściwości EXTENSIONPARAMETER i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="bdcb6-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="bdcb6-136">-ForceRerun</span></span>
<span data-ttu-id="bdcb6-137">W jaki sposób program obsługi rozszerzeń powinien być zmuszony do aktualizacji, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="bdcb6-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdcb6-138">-InputObject</span></span>
<span data-ttu-id="bdcb6-139">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bdcb6-140">-NazwaKomputera</span><span class="sxs-lookup"><span data-stu-id="bdcb6-140">-MachineName</span></span>
<span data-ttu-id="bdcb6-141">Nazwa komputera, na którym ma zostać utworzone lub zaktualizowane rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="bdcb6-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdcb6-142">-Name</span></span>
<span data-ttu-id="bdcb6-143">Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="bdcb6-144">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bdcb6-144">-NoWait</span></span>
<span data-ttu-id="bdcb6-145">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="bdcb6-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bdcb6-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="bdcb6-146">-ProtectedSetting</span></span>
<span data-ttu-id="bdcb6-147">Rozszerzenie może zawierać protectedSettings lub protectedSettingsFromKeyVault lub nie ma żadnych ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="bdcb6-148">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="bdcb6-148">-Publisher</span></span>
<span data-ttu-id="bdcb6-149">Nazwa wydawcy obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="bdcb6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcb6-150">-ResourceGroupName</span></span>
<span data-ttu-id="bdcb6-151">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdcb6-152">-Setting</span><span class="sxs-lookup"><span data-stu-id="bdcb6-152">-Setting</span></span>
<span data-ttu-id="bdcb6-153">Ustawienia publiczne w formacie JSON dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="bdcb6-154">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bdcb6-154">-SubscriptionId</span></span>
<span data-ttu-id="bdcb6-155">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bdcb6-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bdcb6-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="bdcb6-157">-Tag</span></span>
<span data-ttu-id="bdcb6-158">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="bdcb6-158">Resource tags</span></span>

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

### <span data-ttu-id="bdcb6-159">-Type</span><span class="sxs-lookup"><span data-stu-id="bdcb6-159">-Type</span></span>
<span data-ttu-id="bdcb6-160">Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="bdcb6-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="bdcb6-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bdcb6-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="bdcb6-162">Określa wersję obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="bdcb6-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdcb6-163">-Confirm</span></span>
<span data-ttu-id="bdcb6-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdcb6-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdcb6-165">-WhatIf</span></span>
<span data-ttu-id="bdcb6-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdcb6-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdcb6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcb6-168">CommonParameters</span></span>
<span data-ttu-id="bdcb6-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcb6-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdcb6-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcb6-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdcb6-171">INPUTS</span></span>

### <span data-ttu-id="bdcb6-172">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="bdcb6-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="bdcb6-173">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="bdcb6-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="bdcb6-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdcb6-174">OUTPUTS</span></span>

### <span data-ttu-id="bdcb6-175">Microsoft. Azure. PowerShell. polecenia. ConnectedMachine. models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bdcb6-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="bdcb6-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdcb6-176">NOTES</span></span>

<span data-ttu-id="bdcb6-177">PISUJE</span><span class="sxs-lookup"><span data-stu-id="bdcb6-177">ALIASES</span></span>

<span data-ttu-id="bdcb6-178">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdcb6-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bdcb6-179">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdcb6-180">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bdcb6-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : zawiera opis aktualizacji rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="bdcb6-182">`[Tag <IUpdateResourceTags>]`: Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="bdcb6-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="bdcb6-183">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bdcb6-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Wskazuje, czy rozszerzenie ma używać nowszej wersji pomocniczej, jeśli jest dostępna w czasie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="bdcb6-185">Po wdrożeniu rozszerzenie nie będzie jednak uaktualnić wersji pomocniczych, o ile nie zostanie ponownie wdrożone, nawet jeśli ta właściwość ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="bdcb6-186">`[ForceUpdateTag <String>]`: Jak należy wymusić aktualizację procedury obsługi rozszerzeń, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="bdcb6-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Rozszerzenie może zawierać co najmniej protectedSettings lub protectedSettingsFromKeyVault lub bez ustawień chronionych.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="bdcb6-188">`[Publisher <String>]`: Nazwa wydawcy obsługi rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="bdcb6-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Ustawienia publiczne w formacie JSON dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="bdcb6-190">`[Type <String>]`: Określa typ rozszerzenia; Przykładem jest "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="bdcb6-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="bdcb6-191">`[TypeHandlerVersion <String>]`: Określa wersję obsługi skryptów.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="bdcb6-192">INPUTobject <IConnectedMachineIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="bdcb6-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bdcb6-193">`[ExtensionName <String>]`: Nazwa rozszerzenia komputera.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="bdcb6-194">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bdcb6-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bdcb6-195">`[Name <String>]`: Nazwa maszyny hybrydowej.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="bdcb6-196">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bdcb6-197">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bdcb6-198">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="bdcb6-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bdcb6-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdcb6-199">RELATED LINKS</span></span>


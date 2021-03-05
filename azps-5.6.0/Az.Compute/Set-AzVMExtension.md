---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: b1c7a45f538c10c2ef6c2f03809a127a21237fc9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980858"
---
# <span data-ttu-id="e4fcf-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e4fcf-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="e4fcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fcf-103">Aktualizuje właściwości rozszerzenia lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="e4fcf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4fcf-104">SYNTAX</span></span>

### <span data-ttu-id="e4fcf-105">Ustawienia (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e4fcf-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4fcf-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="e4fcf-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4fcf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4fcf-107">DESCRIPTION</span></span>
<span data-ttu-id="e4fcf-108">Polecenie **cmdlet Set-AzVMExtension** aktualizuje właściwości istniejących rozszerzeń maszyn wirtualnych lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="e4fcf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4fcf-109">EXAMPLES</span></span>

### <span data-ttu-id="e4fcf-110">Przykład 1. Modyfikowanie ustawień za pomocą skrótów tabel</span><span class="sxs-lookup"><span data-stu-id="e4fcf-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="e4fcf-111">Pierwsze dwa polecenia używają standardowej składni programu Windows PowerShell do tworzenia tabel skrótów, a następnie przechowuje te tabele skrótów w $Settings i $ProtectedSettings zmiennych.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="e4fcf-112">Aby uzyskać więcej informacji, wpisz `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="e4fcf-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="e4fcf-113">Drugie polecenie zawiera dwie wartości utworzone wcześniej i przechowywane w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="e4fcf-114">Ostatnie polecenie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w grupie Zasobów11 zgodnie z zawartością $Settings i $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="e4fcf-115">To polecenie określa inne wymagane informacje, takie jak wydawca i typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="e4fcf-116">Przykład 2. Modyfikowanie ustawień przy użyciu ciągów</span><span class="sxs-lookup"><span data-stu-id="e4fcf-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="e4fcf-117">Pierwsze dwa polecenia tworzą ciągi zawierające ustawienia, a następnie przechowywają je w $SettingsString i $ProtectedSettingsString zmiennych.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="e4fcf-118">Ostatnie polecenie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w grupie Zasobów11 zgodnie z zawartością $SettingsString i $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="e4fcf-119">To polecenie określa inne wymagane informacje, takie jak wydawca i typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="e4fcf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4fcf-120">PARAMETERS</span></span>

### <span data-ttu-id="e4fcf-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e4fcf-121">-AsJob</span></span>
<span data-ttu-id="e4fcf-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e4fcf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4fcf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fcf-123">-DefaultProfile</span></span>
<span data-ttu-id="e4fcf-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e4fcf-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e4fcf-126">Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa Azure automatyczne aktualizowanie rozszerzeń do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="e4fcf-127">To polecenie cmdlet domyślnie umożliwia agentowi gościowi aktualizowanie rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="e4fcf-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="e4fcf-129">Wskazuje, czy rozszerzenie powinno zostać automatycznie uaktualnione przez platformę, jeśli jest dostępna nowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e4fcf-130">-ExtensionType</span></span>
<span data-ttu-id="e4fcf-131">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-131">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="e4fcf-132">-ForceRerun</span></span>
<span data-ttu-id="e4fcf-133">Wskazuje, że to polecenie cmdlet wymusza ponowne uruchomić tę samą konfigurację rozszerzenia na komputerze wirtualnym bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="e4fcf-134">Wartość może być dowolnym ciągiem innym niż bieżąca wartość.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="e4fcf-135">Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal stosuje aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4fcf-136">-Location</span></span>
<span data-ttu-id="e4fcf-137">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-137">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e4fcf-138">-Name</span></span>
<span data-ttu-id="e4fcf-139">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-139">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e4fcf-140">-NoWait</span></span>
<span data-ttu-id="e4fcf-141">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e4fcf-142">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e4fcf-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="e4fcf-143">-ProtectedSettings</span></span>
<span data-ttu-id="e4fcf-144">Określa konfigurację prywatną rozszerzenia jako tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="e4fcf-145">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-145">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="e4fcf-146">-ProtectedSettingString</span></span>
<span data-ttu-id="e4fcf-147">Określa prywatną konfigurację rozszerzenia jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="e4fcf-148">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-148">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-149">— Publisher</span><span class="sxs-lookup"><span data-stu-id="e4fcf-149">-Publisher</span></span>
<span data-ttu-id="e4fcf-150">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="e4fcf-151">Po zarejestrowaniu rozszerzenia wydawca podaje jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-151">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4fcf-152">-ResourceGroupName</span></span>
<span data-ttu-id="e4fcf-153">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-153">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-154">— Ustawienia</span><span class="sxs-lookup"><span data-stu-id="e4fcf-154">-Settings</span></span>
<span data-ttu-id="e4fcf-155">Określa konfigurację publiczną rozszerzenia jako tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="e4fcf-156">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-156">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="e4fcf-157">-SettingString</span></span>
<span data-ttu-id="e4fcf-158">Określa publiczną konfigurację rozszerzenia jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="e4fcf-159">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-159">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e4fcf-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="e4fcf-161">Określa wersję rozszerzenia do użycia dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-161">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-162">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="e4fcf-162">-VMName</span></span>
<span data-ttu-id="e4fcf-163">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e4fcf-164">To polecenie cmdlet modyfikuje rozszerzenia dla maszyny wirtualnej, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4fcf-165">-Confirm</span></span>
<span data-ttu-id="e4fcf-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4fcf-167">-WhatIf</span></span>
<span data-ttu-id="e4fcf-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4fcf-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4fcf-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fcf-170">CommonParameters</span></span>
<span data-ttu-id="e4fcf-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4fcf-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fcf-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4fcf-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fcf-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4fcf-173">INPUTS</span></span>

### <span data-ttu-id="e4fcf-174">System.String</span><span class="sxs-lookup"><span data-stu-id="e4fcf-174">System.String</span></span>

### <span data-ttu-id="e4fcf-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4fcf-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e4fcf-176">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e4fcf-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e4fcf-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4fcf-177">OUTPUTS</span></span>

### <span data-ttu-id="e4fcf-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e4fcf-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e4fcf-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4fcf-179">NOTES</span></span>

## <span data-ttu-id="e4fcf-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4fcf-180">RELATED LINKS</span></span>

[<span data-ttu-id="e4fcf-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e4fcf-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="e4fcf-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e4fcf-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)



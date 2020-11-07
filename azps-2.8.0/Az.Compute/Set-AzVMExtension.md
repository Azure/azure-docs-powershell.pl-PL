---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: 871323c47cef0b1c2b9d8d1ecc32dc33c5c3b253
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706177"
---
# <span data-ttu-id="56ec6-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="56ec6-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="56ec6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="56ec6-103">Aktualizuje właściwości rozszerzenia lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="56ec6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56ec6-104">SYNTAX</span></span>

### <span data-ttu-id="56ec6-105">Ustawienia (domyślne)</span><span class="sxs-lookup"><span data-stu-id="56ec6-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56ec6-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="56ec6-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56ec6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56ec6-107">DESCRIPTION</span></span>
<span data-ttu-id="56ec6-108">Polecenie cmdlet **Set-AzVMExtension** aktualizuje właściwości istniejących rozszerzeń maszyny wirtualnej lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="56ec6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56ec6-109">EXAMPLES</span></span>

### <span data-ttu-id="56ec6-110">Przykład 1: modyfikowanie ustawień za pomocą tabel skrótów</span><span class="sxs-lookup"><span data-stu-id="56ec6-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="56ec6-111">W dwóch pierwszych poleceniach użyto standardowej składni środowiska Windows PowerShell do tworzenia tabel skrótów, a następnie są one przechowywane w zmiennych $Settings i $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="56ec6-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="56ec6-112">Aby uzyskać więcej informacji, wpisz tekst `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="56ec6-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="56ec6-113">Drugie polecenie zawiera dwie wartości, które zostały wcześniej utworzone i zapisane w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="56ec6-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="56ec6-114">Polecenie ostatnie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11 zgodnie z zawartością $Settings i $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="56ec6-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="56ec6-115">W poleceniu są określone inne wymagane informacje zawierające wydawcę oraz typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="56ec6-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="56ec6-116">Przykład 2: modyfikowanie ustawień za pomocą ciągów znaków</span><span class="sxs-lookup"><span data-stu-id="56ec6-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="56ec6-117">Pierwsze dwa polecenia tworzą ciągi zawierające ustawienia, a następnie przechowują je w $SettingsString i $ProtectedSettingsString zmiennych.</span><span class="sxs-lookup"><span data-stu-id="56ec6-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="56ec6-118">Polecenie ostatnie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11 zgodnie z zawartością $SettingsString i $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="56ec6-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="56ec6-119">W poleceniu są określone inne wymagane informacje zawierające wydawcę oraz typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="56ec6-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="56ec6-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56ec6-120">PARAMETERS</span></span>

### <span data-ttu-id="56ec6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56ec6-121">-AsJob</span></span>
<span data-ttu-id="56ec6-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="56ec6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56ec6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ec6-123">-DefaultProfile</span></span>
<span data-ttu-id="56ec6-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56ec6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56ec6-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="56ec6-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="56ec6-126">Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzeń nowszą wersją pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="56ec6-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="56ec6-127">Domyślnie to polecenie cmdlet umożliwia agentowi gościa aktualizowanie rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="56ec6-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="56ec6-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="56ec6-128">-ExtensionType</span></span>
<span data-ttu-id="56ec6-129">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="56ec6-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="56ec6-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="56ec6-130">-ForceRerun</span></span>
<span data-ttu-id="56ec6-131">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="56ec6-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="56ec6-132">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="56ec6-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="56ec6-133">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="56ec6-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="56ec6-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="56ec6-134">-Location</span></span>
<span data-ttu-id="56ec6-135">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="56ec6-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56ec6-136">-Name</span></span>
<span data-ttu-id="56ec6-137">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="56ec6-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="56ec6-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="56ec6-138">-NoWait</span></span>
<span data-ttu-id="56ec6-139">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="56ec6-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="56ec6-140">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="56ec6-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="56ec6-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="56ec6-141">-ProtectedSettings</span></span>
<span data-ttu-id="56ec6-142">Określa prywatną konfigurację rozszerzenia jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="56ec6-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="56ec6-143">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="56ec6-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="56ec6-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="56ec6-144">-ProtectedSettingString</span></span>
<span data-ttu-id="56ec6-145">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="56ec6-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="56ec6-146">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="56ec6-146">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="56ec6-147">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="56ec6-147">-Publisher</span></span>
<span data-ttu-id="56ec6-148">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="56ec6-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="56ec6-149">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="56ec6-149">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="56ec6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ec6-150">-ResourceGroupName</span></span>
<span data-ttu-id="56ec6-151">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="56ec6-152">-Settings (Ustawienia)</span><span class="sxs-lookup"><span data-stu-id="56ec6-152">-Settings</span></span>
<span data-ttu-id="56ec6-153">Określa publiczną konfigurację rozszerzenia jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="56ec6-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="56ec6-154">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="56ec6-155">-SettingString</span><span class="sxs-lookup"><span data-stu-id="56ec6-155">-SettingString</span></span>
<span data-ttu-id="56ec6-156">Określa publiczną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="56ec6-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="56ec6-157">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-157">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="56ec6-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="56ec6-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="56ec6-159">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-159">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="56ec6-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="56ec6-160">-VMName</span></span>
<span data-ttu-id="56ec6-161">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56ec6-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="56ec6-162">To polecenie cmdlet powoduje modyfikację rozszerzeń maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="56ec6-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="56ec6-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56ec6-163">-Confirm</span></span>
<span data-ttu-id="56ec6-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56ec6-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ec6-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ec6-165">-WhatIf</span></span>
<span data-ttu-id="56ec6-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56ec6-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ec6-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56ec6-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ec6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ec6-168">CommonParameters</span></span>
<span data-ttu-id="56ec6-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ec6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ec6-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56ec6-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ec6-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56ec6-171">INPUTS</span></span>

### <span data-ttu-id="56ec6-172">System. String</span><span class="sxs-lookup"><span data-stu-id="56ec6-172">System.String</span></span>

### <span data-ttu-id="56ec6-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="56ec6-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="56ec6-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56ec6-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56ec6-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56ec6-175">OUTPUTS</span></span>

### <span data-ttu-id="56ec6-176">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="56ec6-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="56ec6-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56ec6-177">NOTES</span></span>

## <span data-ttu-id="56ec6-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56ec6-178">RELATED LINKS</span></span>

[<span data-ttu-id="56ec6-179">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="56ec6-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="56ec6-180">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="56ec6-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: c8aa9660be48f5b5eb2b95343c8a11420978448d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893365"
---
# <span data-ttu-id="869f0-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="869f0-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="869f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="869f0-102">SYNOPSIS</span></span>
<span data-ttu-id="869f0-103">Aktualizuje właściwości rozszerzenia lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="869f0-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="869f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="869f0-104">SYNTAX</span></span>

### <span data-ttu-id="869f0-105">Ustawienia (domyślne)</span><span class="sxs-lookup"><span data-stu-id="869f0-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="869f0-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="869f0-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="869f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="869f0-107">DESCRIPTION</span></span>
<span data-ttu-id="869f0-108">Polecenie cmdlet **Set-AzVMExtension** aktualizuje właściwości istniejących rozszerzeń maszyny wirtualnej lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="869f0-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="869f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="869f0-109">EXAMPLES</span></span>

### <span data-ttu-id="869f0-110">Przykład 1: modyfikowanie ustawień za pomocą tabel skrótów</span><span class="sxs-lookup"><span data-stu-id="869f0-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="869f0-111">W dwóch pierwszych poleceniach użyto standardowej składni środowiska Windows PowerShell do tworzenia tabel skrótów, a następnie są one przechowywane w zmiennych $Settings i $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="869f0-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="869f0-112">Aby uzyskać więcej informacji, wpisz tekst `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="869f0-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="869f0-113">Drugie polecenie zawiera dwie wartości, które zostały wcześniej utworzone i zapisane w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="869f0-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="869f0-114">Polecenie ostatnie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11 zgodnie z zawartością $Settings i $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="869f0-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="869f0-115">W poleceniu są określone inne wymagane informacje zawierające wydawcę oraz typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="869f0-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="869f0-116">Przykład 2: modyfikowanie ustawień za pomocą ciągów znaków</span><span class="sxs-lookup"><span data-stu-id="869f0-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="869f0-117">Pierwsze dwa polecenia tworzą ciągi zawierające ustawienia, a następnie przechowują je w $SettingsString i $ProtectedSettingsString zmiennych.</span><span class="sxs-lookup"><span data-stu-id="869f0-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="869f0-118">Polecenie ostatnie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11 zgodnie z zawartością $SettingsString i $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="869f0-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="869f0-119">W poleceniu są określone inne wymagane informacje zawierające wydawcę oraz typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="869f0-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="869f0-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="869f0-120">PARAMETERS</span></span>

### <span data-ttu-id="869f0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="869f0-121">-AsJob</span></span>
<span data-ttu-id="869f0-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="869f0-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869f0-123">-DefaultProfile</span></span>
<span data-ttu-id="869f0-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="869f0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="869f0-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="869f0-126">Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzeń nowszą wersją pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="869f0-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="869f0-127">Domyślnie to polecenie cmdlet umożliwia agentowi gościa aktualizowanie rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="869f0-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="869f0-128">-ExtensionType</span></span>
<span data-ttu-id="869f0-129">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="869f0-129">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="869f0-130">-ForceRerun</span></span>
<span data-ttu-id="869f0-131">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="869f0-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="869f0-132">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="869f0-132">The value can be any string different from the current value.</span></span>

<span data-ttu-id="869f0-133">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="869f0-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="869f0-134">-Location</span></span>
<span data-ttu-id="869f0-135">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="869f0-135">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="869f0-136">-Name</span></span>
<span data-ttu-id="869f0-137">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="869f0-137">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="869f0-138">-ProtectedSettings</span></span>
<span data-ttu-id="869f0-139">Określa prywatną konfigurację rozszerzenia jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="869f0-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="869f0-140">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="869f0-140">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="869f0-141">-ProtectedSettingString</span></span>
<span data-ttu-id="869f0-142">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="869f0-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="869f0-143">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="869f0-143">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-144">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="869f0-144">-Publisher</span></span>
<span data-ttu-id="869f0-145">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="869f0-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="869f0-146">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="869f0-146">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="869f0-147">-ResourceGroupName</span></span>
<span data-ttu-id="869f0-148">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="869f0-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-149">-Settings (Ustawienia)</span><span class="sxs-lookup"><span data-stu-id="869f0-149">-Settings</span></span>
<span data-ttu-id="869f0-150">Określa publiczną konfigurację rozszerzenia jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="869f0-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="869f0-151">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="869f0-151">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-152">-SettingString</span><span class="sxs-lookup"><span data-stu-id="869f0-152">-SettingString</span></span>
<span data-ttu-id="869f0-153">Określa publiczną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="869f0-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="869f0-154">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="869f0-154">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="869f0-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="869f0-156">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="869f0-156">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="869f0-157">-VMName</span></span>
<span data-ttu-id="869f0-158">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="869f0-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="869f0-159">To polecenie cmdlet powoduje modyfikację rozszerzeń maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="869f0-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="869f0-160">-Confirm</span></span>
<span data-ttu-id="869f0-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="869f0-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="869f0-162">-WhatIf</span></span>
<span data-ttu-id="869f0-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="869f0-163">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="869f0-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="869f0-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="869f0-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869f0-165">CommonParameters</span></span>
<span data-ttu-id="869f0-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869f0-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869f0-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869f0-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869f0-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="869f0-168">INPUTS</span></span>

### <span data-ttu-id="869f0-169">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="869f0-169">None</span></span>
<span data-ttu-id="869f0-170">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="869f0-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="869f0-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="869f0-171">OUTPUTS</span></span>

### <span data-ttu-id="869f0-172">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="869f0-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="869f0-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="869f0-173">NOTES</span></span>

## <span data-ttu-id="869f0-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="869f0-174">RELATED LINKS</span></span>

[<span data-ttu-id="869f0-175">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="869f0-175">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="869f0-176">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="869f0-176">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)



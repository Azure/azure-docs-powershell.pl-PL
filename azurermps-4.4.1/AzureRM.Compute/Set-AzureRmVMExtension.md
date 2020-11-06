---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546264"
---
# <span data-ttu-id="bbecf-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="bbecf-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="bbecf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbecf-102">SYNOPSIS</span></span>
<span data-ttu-id="bbecf-103">Aktualizuje właściwości rozszerzenia lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbecf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbecf-104">SYNTAX</span></span>

### <span data-ttu-id="bbecf-105">Ustawienia (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bbecf-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbecf-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="bbecf-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbecf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bbecf-107">DESCRIPTION</span></span>
<span data-ttu-id="bbecf-108">Polecenie cmdlet **Set-AzureRmVMExtension** aktualizuje właściwości istniejących rozszerzeń maszyny wirtualnej lub dodaje rozszerzenie do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="bbecf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbecf-109">EXAMPLES</span></span>

### <span data-ttu-id="bbecf-110">Przykład 1: modyfikowanie ustawień za pomocą tabel skrótów</span><span class="sxs-lookup"><span data-stu-id="bbecf-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="bbecf-111">W dwóch pierwszych poleceniach użyto standardowej składni środowiska Windows PowerShell do tworzenia tabel skrótów, a następnie są one przechowywane w zmiennych $Settings i $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="bbecf-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="bbecf-112">Aby uzyskać więcej informacji, wpisz tekst `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="bbecf-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="bbecf-113">Drugie polecenie zawiera dwie wartości, które zostały wcześniej utworzone i zapisane w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="bbecf-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="bbecf-114">Polecenie ostatnie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11 zgodnie z zawartością $Settings i $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="bbecf-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="bbecf-115">W poleceniu są określone inne wymagane informacje zawierające wydawcę oraz typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bbecf-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="bbecf-116">Przykład 2: modyfikowanie ustawień za pomocą ciągów znaków</span><span class="sxs-lookup"><span data-stu-id="bbecf-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="bbecf-117">Pierwsze dwa polecenia tworzą ciągi zawierające ustawienia, a następnie przechowują je w $SettingsString i $ProtectedSettingsString zmiennych.</span><span class="sxs-lookup"><span data-stu-id="bbecf-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="bbecf-118">Polecenie ostatnie modyfikuje rozszerzenie maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11 zgodnie z zawartością $SettingsString i $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="bbecf-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="bbecf-119">W poleceniu są określone inne wymagane informacje zawierające wydawcę oraz typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bbecf-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="bbecf-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbecf-120">PARAMETERS</span></span>

### <span data-ttu-id="bbecf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbecf-121">-DefaultProfile</span></span>
<span data-ttu-id="bbecf-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbecf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbecf-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bbecf-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bbecf-124">Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzeń nowszą wersją pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="bbecf-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="bbecf-125">Domyślnie to polecenie cmdlet umożliwia agentowi gościa aktualizowanie rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="bbecf-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="bbecf-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="bbecf-126">-ExtensionType</span></span>
<span data-ttu-id="bbecf-127">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bbecf-127">Specifies the extension type.</span></span>

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

### <span data-ttu-id="bbecf-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="bbecf-128">-ForceRerun</span></span>
<span data-ttu-id="bbecf-129">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bbecf-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="bbecf-130">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="bbecf-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="bbecf-131">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="bbecf-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="bbecf-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bbecf-132">-Location</span></span>
<span data-ttu-id="bbecf-133">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="bbecf-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bbecf-134">-Name</span></span>
<span data-ttu-id="bbecf-135">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bbecf-135">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="bbecf-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="bbecf-136">-ProtectedSettings</span></span>
<span data-ttu-id="bbecf-137">Określa prywatną konfigurację rozszerzenia jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="bbecf-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="bbecf-138">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="bbecf-138">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="bbecf-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="bbecf-139">-ProtectedSettingString</span></span>
<span data-ttu-id="bbecf-140">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="bbecf-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="bbecf-141">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="bbecf-141">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="bbecf-142">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="bbecf-142">-Publisher</span></span>
<span data-ttu-id="bbecf-143">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bbecf-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="bbecf-144">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="bbecf-144">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="bbecf-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbecf-145">-ResourceGroupName</span></span>
<span data-ttu-id="bbecf-146">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bbecf-147">-Settings (Ustawienia)</span><span class="sxs-lookup"><span data-stu-id="bbecf-147">-Settings</span></span>
<span data-ttu-id="bbecf-148">Określa publiczną konfigurację rozszerzenia jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="bbecf-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="bbecf-149">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-149">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="bbecf-150">-SettingString</span><span class="sxs-lookup"><span data-stu-id="bbecf-150">-SettingString</span></span>
<span data-ttu-id="bbecf-151">Określa publiczną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="bbecf-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="bbecf-152">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-152">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="bbecf-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bbecf-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="bbecf-154">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-154">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="bbecf-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="bbecf-155">-VMName</span></span>
<span data-ttu-id="bbecf-156">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bbecf-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="bbecf-157">To polecenie cmdlet powoduje modyfikację rozszerzeń maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bbecf-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbecf-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbecf-158">-Confirm</span></span>
<span data-ttu-id="bbecf-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbecf-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbecf-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbecf-160">-WhatIf</span></span>
<span data-ttu-id="bbecf-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbecf-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bbecf-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbecf-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbecf-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbecf-163">CommonParameters</span></span>
<span data-ttu-id="bbecf-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbecf-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbecf-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbecf-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbecf-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbecf-166">INPUTS</span></span>

## <span data-ttu-id="bbecf-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbecf-167">OUTPUTS</span></span>

## <span data-ttu-id="bbecf-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbecf-168">NOTES</span></span>

## <span data-ttu-id="bbecf-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbecf-169">RELATED LINKS</span></span>

[<span data-ttu-id="bbecf-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="bbecf-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="bbecf-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="bbecf-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)



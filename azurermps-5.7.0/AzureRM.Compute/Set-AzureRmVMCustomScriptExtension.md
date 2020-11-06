---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 693809e46823cbcb8331eade7b8cd38c83238be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542695"
---
# <span data-ttu-id="95a16-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="95a16-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="95a16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95a16-102">SYNOPSIS</span></span>
<span data-ttu-id="95a16-103">Umożliwia dodanie niestandardowego rozszerzenia skryptu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a16-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95a16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95a16-104">SYNTAX</span></span>

### <span data-ttu-id="95a16-105">SetCustomScriptExtensionByContainerAndFileNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="95a16-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95a16-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="95a16-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95a16-107">Opis</span><span class="sxs-lookup"><span data-stu-id="95a16-107">DESCRIPTION</span></span>
<span data-ttu-id="95a16-108">Polecenie cmdlet **Set-AzureRmVMCustomScriptExtension** dodaje rozszerzenie maszyny wirtualnej skryptu niestandardowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a16-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="95a16-109">To rozszerzenie umożliwia uruchamianie własnych skryptów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a16-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="95a16-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95a16-110">EXAMPLES</span></span>

### <span data-ttu-id="95a16-111">Przykład 1: Dodawanie skryptu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="95a16-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="95a16-112">To polecenie umożliwia dodanie niestandardowego skryptu do maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="95a16-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="95a16-113">Plik skryptu jest contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="95a16-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="95a16-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95a16-114">PARAMETERS</span></span>

### <span data-ttu-id="95a16-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="95a16-115">-Argument</span></span>
<span data-ttu-id="95a16-116">Określa argumenty, które rozszerzenie skryptu przekazuje do skryptu.</span><span class="sxs-lookup"><span data-stu-id="95a16-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="95a16-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="95a16-117">-ContainerName</span></span>
<span data-ttu-id="95a16-118">Określa nazwę kontenera magazynu platformy Azure, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="95a16-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a16-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="95a16-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="95a16-120">-FileName</span><span class="sxs-lookup"><span data-stu-id="95a16-120">-FileName</span></span>
<span data-ttu-id="95a16-121">Określa nazwę pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="95a16-121">Specifies the name of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a16-122">-FileUri</span><span class="sxs-lookup"><span data-stu-id="95a16-122">-FileUri</span></span>
<span data-ttu-id="95a16-123">Określa identyfikator URI pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="95a16-123">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a16-124">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="95a16-124">-ForceRerun</span></span>
<span data-ttu-id="95a16-125">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="95a16-125">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="95a16-126">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="95a16-126">The value can be any string different from the current value.</span></span>

<span data-ttu-id="95a16-127">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="95a16-127">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="95a16-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="95a16-128">-Location</span></span>
<span data-ttu-id="95a16-129">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a16-129">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="95a16-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95a16-130">-Name</span></span>
<span data-ttu-id="95a16-131">Określa nazwę niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="95a16-131">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="95a16-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95a16-132">-ResourceGroupName</span></span>
<span data-ttu-id="95a16-133">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a16-133">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="95a16-134">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="95a16-134">-Run</span></span>
<span data-ttu-id="95a16-135">Określa polecenie, którego należy użyć w celu uruchomienia skryptu.</span><span class="sxs-lookup"><span data-stu-id="95a16-135">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a16-136">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="95a16-136">-SecureExecution</span></span>
<span data-ttu-id="95a16-137">Wskazuje, że ten aplet polecenia sprawdza, czy wartość parametru *uruchomienia* nie jest rejestrowana na serwerze ani zwracana do użytkownika przy użyciu interfejsu API pobierania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="95a16-137">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="95a16-138">Wartość w polu *Uruchom* może zawierać klucze tajne lub hasła, które są bezpiecznie przekazywane do pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="95a16-138">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="95a16-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="95a16-139">-StorageAccountKey</span></span>
<span data-ttu-id="95a16-140">Określa klucz kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95a16-140">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a16-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="95a16-141">-StorageAccountName</span></span>
<span data-ttu-id="95a16-142">Określa nazwę konta usługi Azure Storage, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="95a16-142">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a16-143">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="95a16-143">-StorageEndpointSuffix</span></span>
<span data-ttu-id="95a16-144">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="95a16-144">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95a16-145">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="95a16-145">-TypeHandlerVersion</span></span>
<span data-ttu-id="95a16-146">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a16-146">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="95a16-147">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzureRmVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="95a16-147">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="95a16-148">-VMName</span><span class="sxs-lookup"><span data-stu-id="95a16-148">-VMName</span></span>
<span data-ttu-id="95a16-149">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95a16-149">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="95a16-150">To polecenie cmdlet umożliwia dodanie niestandardowego rozszerzenia skryptu dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="95a16-150">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="95a16-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95a16-151">-Confirm</span></span>
<span data-ttu-id="95a16-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95a16-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95a16-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95a16-153">-WhatIf</span></span>
<span data-ttu-id="95a16-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95a16-154">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="95a16-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="95a16-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95a16-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a16-156">CommonParameters</span></span>
<span data-ttu-id="95a16-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a16-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a16-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a16-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a16-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95a16-159">INPUTS</span></span>

### <span data-ttu-id="95a16-160">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="95a16-160">None</span></span>
<span data-ttu-id="95a16-161">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="95a16-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95a16-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95a16-162">OUTPUTS</span></span>

## <span data-ttu-id="95a16-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95a16-163">NOTES</span></span>

## <span data-ttu-id="95a16-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95a16-164">RELATED LINKS</span></span>

[<span data-ttu-id="95a16-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="95a16-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="95a16-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="95a16-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 6fe34ae33ed70cebe4c8f76beb235e6fa7445fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893389"
---
# <span data-ttu-id="64d67-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="64d67-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="64d67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64d67-102">SYNOPSIS</span></span>
<span data-ttu-id="64d67-103">Umożliwia dodanie niestandardowego rozszerzenia skryptu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64d67-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="64d67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64d67-104">SYNTAX</span></span>

### <span data-ttu-id="64d67-105">SetCustomScriptExtensionByContainerAndFileNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64d67-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d67-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="64d67-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d67-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64d67-107">DESCRIPTION</span></span>
<span data-ttu-id="64d67-108">Polecenie cmdlet **Set-AzVMCustomScriptExtension** dodaje rozszerzenie maszyny wirtualnej skryptu niestandardowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64d67-108">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="64d67-109">To rozszerzenie umożliwia uruchamianie własnych skryptów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64d67-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="64d67-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64d67-110">EXAMPLES</span></span>

### <span data-ttu-id="64d67-111">Przykład 1: Dodawanie skryptu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="64d67-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="64d67-112">To polecenie umożliwia dodanie niestandardowego skryptu do maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="64d67-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="64d67-113">Plik skryptu jest contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="64d67-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="64d67-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64d67-114">PARAMETERS</span></span>

### <span data-ttu-id="64d67-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="64d67-115">-Argument</span></span>
<span data-ttu-id="64d67-116">Określa argumenty, które rozszerzenie skryptu przekazuje do skryptu.</span><span class="sxs-lookup"><span data-stu-id="64d67-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="64d67-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="64d67-117">-ContainerName</span></span>
<span data-ttu-id="64d67-118">Określa nazwę kontenera magazynu platformy Azure, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="64d67-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="64d67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d67-119">-DefaultProfile</span></span>
<span data-ttu-id="64d67-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64d67-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d67-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="64d67-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="64d67-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="64d67-122">-FileName</span></span>
<span data-ttu-id="64d67-123">Określa nazwę pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="64d67-123">Specifies the name of the script file.</span></span> <span data-ttu-id="64d67-124">Jeśli plik jest przechowywany w usłudze Azure Blob Storage, w polu Nazwa pliku jest uwzględniana wartość senstive.</span><span class="sxs-lookup"><span data-stu-id="64d67-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="64d67-125">Nazwy plików plików przechowywanych w usłudze Azure File Storage nie są rozróżniane senstive.</span><span class="sxs-lookup"><span data-stu-id="64d67-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

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

### <span data-ttu-id="64d67-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="64d67-126">-FileUri</span></span>
<span data-ttu-id="64d67-127">Określa identyfikator URI pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="64d67-127">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="64d67-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="64d67-128">-ForceRerun</span></span>
<span data-ttu-id="64d67-129">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="64d67-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="64d67-130">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="64d67-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="64d67-131">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="64d67-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="64d67-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="64d67-132">-Location</span></span>
<span data-ttu-id="64d67-133">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64d67-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="64d67-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64d67-134">-Name</span></span>
<span data-ttu-id="64d67-135">Określa nazwę niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="64d67-135">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="64d67-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d67-136">-ResourceGroupName</span></span>
<span data-ttu-id="64d67-137">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64d67-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="64d67-138">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="64d67-138">-Run</span></span>
<span data-ttu-id="64d67-139">Określa polecenie, którego należy użyć w celu uruchomienia skryptu.</span><span class="sxs-lookup"><span data-stu-id="64d67-139">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="64d67-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="64d67-140">-SecureExecution</span></span>
<span data-ttu-id="64d67-141">Wskazuje, że ten aplet polecenia sprawdza, czy wartość parametru *uruchomienia* nie jest rejestrowana na serwerze ani zwracana do użytkownika przy użyciu interfejsu API pobierania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="64d67-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="64d67-142">Wartość w polu *Uruchom* może zawierać klucze tajne lub hasła, które są bezpiecznie przekazywane do pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="64d67-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="64d67-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="64d67-143">-StorageAccountKey</span></span>
<span data-ttu-id="64d67-144">Określa klucz kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="64d67-144">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="64d67-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="64d67-145">-StorageAccountName</span></span>
<span data-ttu-id="64d67-146">Określa nazwę konta usługi Azure Storage, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="64d67-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="64d67-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="64d67-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="64d67-148">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="64d67-148">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="64d67-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="64d67-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="64d67-150">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64d67-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="64d67-151">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="64d67-151">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="64d67-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="64d67-152">-VMName</span></span>
<span data-ttu-id="64d67-153">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="64d67-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="64d67-154">To polecenie cmdlet umożliwia dodanie niestandardowego rozszerzenia skryptu dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="64d67-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="64d67-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64d67-155">-Confirm</span></span>
<span data-ttu-id="64d67-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64d67-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d67-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d67-157">-WhatIf</span></span>
<span data-ttu-id="64d67-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64d67-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="64d67-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64d67-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d67-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d67-160">CommonParameters</span></span>
<span data-ttu-id="64d67-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d67-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d67-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d67-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d67-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64d67-163">INPUTS</span></span>

### <span data-ttu-id="64d67-164">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="64d67-164">None</span></span>
<span data-ttu-id="64d67-165">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="64d67-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64d67-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64d67-166">OUTPUTS</span></span>

### <span data-ttu-id="64d67-167">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="64d67-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="64d67-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64d67-168">NOTES</span></span>

## <span data-ttu-id="64d67-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64d67-169">RELATED LINKS</span></span>

[<span data-ttu-id="64d67-170">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="64d67-170">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="64d67-171">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="64d67-171">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)



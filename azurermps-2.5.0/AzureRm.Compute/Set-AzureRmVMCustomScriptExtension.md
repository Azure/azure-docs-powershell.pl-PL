---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 2a3e954d53f18cbc120c9d9acb747b3e332a5512
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897481"
---
# <span data-ttu-id="d72f5-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d72f5-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="d72f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d72f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d72f5-103">Umożliwia dodanie niestandardowego rozszerzenia skryptu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72f5-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d72f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d72f5-104">SYNTAX</span></span>

### <span data-ttu-id="d72f5-105">SetCustomScriptExtensionByContainerAndFileNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d72f5-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72f5-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="d72f5-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72f5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d72f5-107">DESCRIPTION</span></span>
<span data-ttu-id="d72f5-108">Polecenie cmdlet **Set-AzureRmVMCustomScriptExtension** dodaje rozszerzenie maszyny wirtualnej skryptu niestandardowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72f5-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="d72f5-109">To rozszerzenie umożliwia uruchamianie własnych skryptów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72f5-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="d72f5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d72f5-110">EXAMPLES</span></span>

### <span data-ttu-id="d72f5-111">Przykład 1: Dodawanie skryptu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="d72f5-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="d72f5-112">To polecenie umożliwia dodanie niestandardowego skryptu do maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="d72f5-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="d72f5-113">Plik skryptu jest contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="d72f5-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="d72f5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d72f5-114">PARAMETERS</span></span>

### <span data-ttu-id="d72f5-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="d72f5-115">-Argument</span></span>
<span data-ttu-id="d72f5-116">Określa argumenty, które rozszerzenie skryptu przekazuje do skryptu.</span><span class="sxs-lookup"><span data-stu-id="d72f5-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="d72f5-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d72f5-117">-ContainerName</span></span>
<span data-ttu-id="d72f5-118">Określa nazwę kontenera magazynu platformy Azure, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="d72f5-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="d72f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72f5-119">-DefaultProfile</span></span>
<span data-ttu-id="d72f5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d72f5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d72f5-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d72f5-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="d72f5-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="d72f5-122">-FileName</span></span>
<span data-ttu-id="d72f5-123">Określa nazwę pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="d72f5-123">Specifies the name of the script file.</span></span> <span data-ttu-id="d72f5-124">Jeśli plik jest przechowywany w usłudze Azure Blob Storage, w polu Nazwa pliku jest uwzględniana wartość senstive.</span><span class="sxs-lookup"><span data-stu-id="d72f5-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="d72f5-125">Nazwy plików plików przechowywanych w usłudze Azure File Storage nie są rozróżniane senstive.</span><span class="sxs-lookup"><span data-stu-id="d72f5-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

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

### <span data-ttu-id="d72f5-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="d72f5-126">-FileUri</span></span>
<span data-ttu-id="d72f5-127">Określa identyfikator URI pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="d72f5-127">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="d72f5-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d72f5-128">-ForceRerun</span></span>
<span data-ttu-id="d72f5-129">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d72f5-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d72f5-130">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="d72f5-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="d72f5-131">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="d72f5-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d72f5-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d72f5-132">-Location</span></span>
<span data-ttu-id="d72f5-133">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72f5-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d72f5-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d72f5-134">-Name</span></span>
<span data-ttu-id="d72f5-135">Określa nazwę niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="d72f5-135">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="d72f5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72f5-136">-ResourceGroupName</span></span>
<span data-ttu-id="d72f5-137">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72f5-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d72f5-138">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="d72f5-138">-Run</span></span>
<span data-ttu-id="d72f5-139">Określa polecenie, którego należy użyć w celu uruchomienia skryptu.</span><span class="sxs-lookup"><span data-stu-id="d72f5-139">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="d72f5-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="d72f5-140">-SecureExecution</span></span>
<span data-ttu-id="d72f5-141">Wskazuje, że ten aplet polecenia sprawdza, czy wartość parametru *uruchomienia* nie jest rejestrowana na serwerze ani zwracana do użytkownika przy użyciu interfejsu API pobierania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d72f5-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="d72f5-142">Wartość w polu *Uruchom* może zawierać klucze tajne lub hasła, które są bezpiecznie przekazywane do pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="d72f5-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="d72f5-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d72f5-143">-StorageAccountKey</span></span>
<span data-ttu-id="d72f5-144">Określa klucz kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d72f5-144">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="d72f5-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d72f5-145">-StorageAccountName</span></span>
<span data-ttu-id="d72f5-146">Określa nazwę konta usługi Azure Storage, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="d72f5-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="d72f5-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d72f5-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="d72f5-148">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="d72f5-148">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="d72f5-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d72f5-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="d72f5-150">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72f5-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d72f5-151">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzureRmVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="d72f5-151">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="d72f5-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="d72f5-152">-VMName</span></span>
<span data-ttu-id="d72f5-153">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d72f5-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d72f5-154">To polecenie cmdlet umożliwia dodanie niestandardowego rozszerzenia skryptu dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d72f5-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d72f5-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d72f5-155">-Confirm</span></span>
<span data-ttu-id="d72f5-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72f5-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72f5-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72f5-157">-WhatIf</span></span>
<span data-ttu-id="d72f5-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72f5-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d72f5-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d72f5-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72f5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72f5-160">CommonParameters</span></span>
<span data-ttu-id="d72f5-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72f5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72f5-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72f5-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72f5-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d72f5-163">INPUTS</span></span>

### <span data-ttu-id="d72f5-164">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d72f5-164">None</span></span>
<span data-ttu-id="d72f5-165">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d72f5-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d72f5-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d72f5-166">OUTPUTS</span></span>

### <span data-ttu-id="d72f5-167">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d72f5-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d72f5-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d72f5-168">NOTES</span></span>

## <span data-ttu-id="d72f5-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d72f5-169">RELATED LINKS</span></span>

[<span data-ttu-id="d72f5-170">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d72f5-170">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="d72f5-171">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d72f5-171">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)



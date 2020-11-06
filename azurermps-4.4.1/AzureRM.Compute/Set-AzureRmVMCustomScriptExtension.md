---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: a9d03bd7f506c7210eeee90c379f90dd0833818e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525577"
---
# <span data-ttu-id="691a8-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="691a8-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="691a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="691a8-102">SYNOPSIS</span></span>
<span data-ttu-id="691a8-103">Umożliwia dodanie niestandardowego rozszerzenia skryptu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="691a8-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="691a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="691a8-104">SYNTAX</span></span>

### <span data-ttu-id="691a8-105">SetCustomScriptExtensionByContainerAndFileNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="691a8-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="691a8-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="691a8-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="691a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="691a8-107">DESCRIPTION</span></span>
<span data-ttu-id="691a8-108">Polecenie cmdlet **Set-AzureRmVMCustomScriptExtension** dodaje rozszerzenie maszyny wirtualnej skryptu niestandardowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="691a8-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="691a8-109">To rozszerzenie umożliwia uruchamianie własnych skryptów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="691a8-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="691a8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="691a8-110">EXAMPLES</span></span>

### <span data-ttu-id="691a8-111">Przykład 1: Dodawanie skryptu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="691a8-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="691a8-112">To polecenie umożliwia dodanie niestandardowego skryptu do maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="691a8-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="691a8-113">Plik skryptu jest contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="691a8-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="691a8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="691a8-114">PARAMETERS</span></span>

### <span data-ttu-id="691a8-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="691a8-115">-Argument</span></span>
<span data-ttu-id="691a8-116">Określa argumenty, które rozszerzenie skryptu przekazuje do skryptu.</span><span class="sxs-lookup"><span data-stu-id="691a8-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="691a8-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="691a8-117">-ContainerName</span></span>
<span data-ttu-id="691a8-118">Określa nazwę kontenera magazynu platformy Azure, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="691a8-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691a8-119">-DefaultProfile</span></span>
<span data-ttu-id="691a8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="691a8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="691a8-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="691a8-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="691a8-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="691a8-122">-FileName</span></span>
<span data-ttu-id="691a8-123">Określa nazwę pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="691a8-123">Specifies the name of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691a8-124">-FileUri</span><span class="sxs-lookup"><span data-stu-id="691a8-124">-FileUri</span></span>
<span data-ttu-id="691a8-125">Określa identyfikator URI pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="691a8-125">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691a8-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="691a8-126">-ForceRerun</span></span>
<span data-ttu-id="691a8-127">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="691a8-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="691a8-128">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="691a8-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="691a8-129">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="691a8-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="691a8-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="691a8-130">-Location</span></span>
<span data-ttu-id="691a8-131">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="691a8-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="691a8-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="691a8-132">-Name</span></span>
<span data-ttu-id="691a8-133">Określa nazwę niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="691a8-133">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="691a8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="691a8-134">-ResourceGroupName</span></span>
<span data-ttu-id="691a8-135">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="691a8-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="691a8-136">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="691a8-136">-Run</span></span>
<span data-ttu-id="691a8-137">Określa polecenie, którego należy użyć w celu uruchomienia skryptu.</span><span class="sxs-lookup"><span data-stu-id="691a8-137">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691a8-138">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="691a8-138">-SecureExecution</span></span>
<span data-ttu-id="691a8-139">Wskazuje, że ten aplet polecenia sprawdza, czy wartość parametru *uruchomienia* nie jest rejestrowana na serwerze ani zwracana do użytkownika przy użyciu interfejsu API pobierania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="691a8-139">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="691a8-140">Wartość w polu *Uruchom* może zawierać klucze tajne lub hasła, które są bezpiecznie przekazywane do pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="691a8-140">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="691a8-141">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="691a8-141">-StorageAccountKey</span></span>
<span data-ttu-id="691a8-142">Określa klucz kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="691a8-142">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691a8-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="691a8-143">-StorageAccountName</span></span>
<span data-ttu-id="691a8-144">Określa nazwę konta usługi Azure Storage, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="691a8-144">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691a8-145">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="691a8-145">-StorageEndpointSuffix</span></span>
<span data-ttu-id="691a8-146">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="691a8-146">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="691a8-147">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="691a8-147">-TypeHandlerVersion</span></span>
<span data-ttu-id="691a8-148">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="691a8-148">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="691a8-149">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzureRmVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="691a8-149">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="691a8-150">-VMName</span><span class="sxs-lookup"><span data-stu-id="691a8-150">-VMName</span></span>
<span data-ttu-id="691a8-151">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="691a8-151">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="691a8-152">To polecenie cmdlet umożliwia dodanie niestandardowego rozszerzenia skryptu dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="691a8-152">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="691a8-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="691a8-153">-Confirm</span></span>
<span data-ttu-id="691a8-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="691a8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="691a8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="691a8-155">-WhatIf</span></span>
<span data-ttu-id="691a8-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="691a8-156">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="691a8-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="691a8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="691a8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691a8-158">CommonParameters</span></span>
<span data-ttu-id="691a8-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="691a8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691a8-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691a8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691a8-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="691a8-161">INPUTS</span></span>

## <span data-ttu-id="691a8-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="691a8-162">OUTPUTS</span></span>

## <span data-ttu-id="691a8-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="691a8-163">NOTES</span></span>

## <span data-ttu-id="691a8-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="691a8-164">RELATED LINKS</span></span>

[<span data-ttu-id="691a8-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="691a8-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="691a8-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="691a8-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)



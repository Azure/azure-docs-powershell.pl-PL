---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 4ed63b1afa2f72e8f557cc95381883973ae7feb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053604"
---
# <span data-ttu-id="ff284-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ff284-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="ff284-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff284-102">SYNOPSIS</span></span>
<span data-ttu-id="ff284-103">Umożliwia dodanie niestandardowego rozszerzenia skryptu do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="ff284-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff284-104">SYNTAX</span></span>

### <span data-ttu-id="ff284-105">ByNameWithContainerAndFileNamesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff284-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff284-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff284-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff284-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff284-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff284-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff284-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff284-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff284-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff284-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff284-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff284-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff284-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff284-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff284-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff284-113">Opis</span><span class="sxs-lookup"><span data-stu-id="ff284-113">DESCRIPTION</span></span>
<span data-ttu-id="ff284-114">Polecenie cmdlet **Set-AzVMCustomScriptExtension** dodaje rozszerzenie maszyny wirtualnej skryptu niestandardowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="ff284-115">To rozszerzenie umożliwia uruchamianie własnych skryptów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="ff284-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff284-116">EXAMPLES</span></span>

### <span data-ttu-id="ff284-117">Przykład 1: Dodawanie skryptu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="ff284-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="ff284-118">To polecenie umożliwia dodanie niestandardowego skryptu do maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ff284-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ff284-119">Plik skryptu jest contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="ff284-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="ff284-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff284-120">PARAMETERS</span></span>

### <span data-ttu-id="ff284-121">-Argument</span><span class="sxs-lookup"><span data-stu-id="ff284-121">-Argument</span></span>
<span data-ttu-id="ff284-122">Określa argumenty, które rozszerzenie skryptu przekazuje do skryptu.</span><span class="sxs-lookup"><span data-stu-id="ff284-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="ff284-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ff284-123">-ContainerName</span></span>
<span data-ttu-id="ff284-124">Określa nazwę kontenera magazynu platformy Azure, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="ff284-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff284-125">-DefaultProfile</span></span>
<span data-ttu-id="ff284-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff284-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff284-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ff284-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="ff284-128">-FileName</span><span class="sxs-lookup"><span data-stu-id="ff284-128">-FileName</span></span>
<span data-ttu-id="ff284-129">Określa nazwę pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="ff284-129">Specifies the name of the script file.</span></span> <span data-ttu-id="ff284-130">Jeśli plik jest przechowywany w usłudze Azure Blob Storage, w wartości nazwy pliku jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ff284-130">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="ff284-131">W nazwach plików przechowywanych w usłudze Azure File Storage nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ff284-131">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="ff284-132">-FileUri</span></span>
<span data-ttu-id="ff284-133">Określa identyfikator URI pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="ff284-133">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ff284-134">-ForceRerun</span></span>
<span data-ttu-id="ff284-135">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ff284-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ff284-136">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="ff284-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="ff284-137">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="ff284-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ff284-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ff284-138">-InputObject</span></span>
<span data-ttu-id="ff284-139">Obiekt rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-139">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-140">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ff284-140">-Location</span></span>
<span data-ttu-id="ff284-141">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ff284-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff284-142">-Name</span></span>
<span data-ttu-id="ff284-143">Określa nazwę niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="ff284-143">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-144">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ff284-144">-NoWait</span></span>
<span data-ttu-id="ff284-145">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="ff284-145">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ff284-146">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="ff284-146">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ff284-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff284-147">-ResourceGroupName</span></span>
<span data-ttu-id="ff284-148">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff284-149">-ResourceId</span></span>
<span data-ttu-id="ff284-150">Identyfikator zasobu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-150">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-151">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="ff284-151">-Run</span></span>
<span data-ttu-id="ff284-152">Określa polecenie, którego należy użyć w celu uruchomienia skryptu.</span><span class="sxs-lookup"><span data-stu-id="ff284-152">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="ff284-153">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="ff284-153">-SecureExecution</span></span>
<span data-ttu-id="ff284-154">Wskazuje, że ten aplet polecenia sprawdza, czy wartość parametru *uruchomienia* nie jest rejestrowana na serwerze ani zwracana do użytkownika przy użyciu interfejsu API pobierania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ff284-154">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="ff284-155">Wartość w polu *Uruchom* może zawierać klucze tajne lub hasła, które są bezpiecznie przekazywane do pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="ff284-155">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="ff284-156">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff284-156">-StorageAccountKey</span></span>
<span data-ttu-id="ff284-157">Określa klucz kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff284-157">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-158">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff284-158">-StorageAccountName</span></span>
<span data-ttu-id="ff284-159">Określa nazwę konta usługi Azure Storage, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="ff284-159">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-160">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ff284-160">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ff284-161">Określa sufiks punktu końcowego składowania.</span><span class="sxs-lookup"><span data-stu-id="ff284-161">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-162">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ff284-162">-TypeHandlerVersion</span></span>
<span data-ttu-id="ff284-163">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-163">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ff284-164">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i CustomScriptExtension dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="ff284-164">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="ff284-165">-VMName</span><span class="sxs-lookup"><span data-stu-id="ff284-165">-VMName</span></span>
<span data-ttu-id="ff284-166">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-166">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ff284-167">To polecenie cmdlet umożliwia dodanie niestandardowego rozszerzenia skryptu dla maszyny wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="ff284-167">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-168">-VMObject</span><span class="sxs-lookup"><span data-stu-id="ff284-168">-VMObject</span></span>
<span data-ttu-id="ff284-169">Obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff284-169">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff284-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff284-170">-Confirm</span></span>
<span data-ttu-id="ff284-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff284-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff284-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff284-172">-WhatIf</span></span>
<span data-ttu-id="ff284-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff284-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff284-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff284-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff284-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff284-175">CommonParameters</span></span>
<span data-ttu-id="ff284-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff284-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff284-177">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff284-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff284-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff284-178">INPUTS</span></span>

### <span data-ttu-id="ff284-179">System. String</span><span class="sxs-lookup"><span data-stu-id="ff284-179">System.String</span></span>

### <span data-ttu-id="ff284-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="ff284-180">System.String[]</span></span>

### <span data-ttu-id="ff284-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ff284-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ff284-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff284-182">OUTPUTS</span></span>

### <span data-ttu-id="ff284-183">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ff284-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ff284-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff284-184">NOTES</span></span>

## <span data-ttu-id="ff284-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff284-185">RELATED LINKS</span></span>

[<span data-ttu-id="ff284-186">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ff284-186">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="ff284-187">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ff284-187">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)



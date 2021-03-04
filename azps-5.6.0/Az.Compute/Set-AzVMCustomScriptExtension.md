---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 97f2c22d4e724d53c165e2e1e73ba27fce9290b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957553"
---
# <span data-ttu-id="f7747-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f7747-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="f7747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7747-102">SYNOPSIS</span></span>
<span data-ttu-id="f7747-103">Dodaje rozszerzenie skryptu niestandardowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7747-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="f7747-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f7747-104">SYNTAX</span></span>

### <span data-ttu-id="f7747-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="f7747-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7747-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7747-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7747-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7747-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7747-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7747-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7747-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7747-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7747-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7747-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7747-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7747-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7747-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7747-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7747-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="f7747-113">DESCRIPTION</span></span>
<span data-ttu-id="f7747-114">Polecenie **cmdlet Set-AzVMCustomScriptExtension** dodaje do maszyny wirtualnej niestandardowe rozszerzenie skryptu Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="f7747-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="f7747-115">To rozszerzenie umożliwia uruchamianie własnych skryptów na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="f7747-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="f7747-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f7747-116">EXAMPLES</span></span>

### <span data-ttu-id="f7747-117">Przykład 1. Dodawanie skryptu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="f7747-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="f7747-118">To polecenie powoduje dodanie do maszyny wirtualnej skryptu niestandardowego o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="f7747-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="f7747-119">Plik skryptu jest contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="f7747-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="f7747-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f7747-120">Example 2</span></span>

<span data-ttu-id="f7747-121">Dodaje rozszerzenie skryptu niestandardowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7747-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="f7747-122">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="f7747-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="f7747-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7747-123">PARAMETERS</span></span>

### <span data-ttu-id="f7747-124">— argument</span><span class="sxs-lookup"><span data-stu-id="f7747-124">-Argument</span></span>
<span data-ttu-id="f7747-125">Określa argumenty, które rozszerzenie skryptu przekazuje do skryptu.</span><span class="sxs-lookup"><span data-stu-id="f7747-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="f7747-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f7747-126">-ContainerName</span></span>
<span data-ttu-id="f7747-127">Określa nazwę kontenera magazynu platformy Azure, w którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="f7747-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="f7747-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7747-128">-DefaultProfile</span></span>
<span data-ttu-id="f7747-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7747-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7747-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f7747-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="f7747-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="f7747-131">-FileName</span></span>
<span data-ttu-id="f7747-132">Określa nazwę pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="f7747-132">Specifies the name of the script file.</span></span> <span data-ttu-id="f7747-133">Jeśli plik jest przechowywany w magazynie obiektów blob platformy Azure, w nazwie pliku jest zróżnicowany wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f7747-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="f7747-134">W nazwach plików przechowywanych w magazynie plików platformy Azure nie jest wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="f7747-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="f7747-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="f7747-135">-FileUri</span></span>
<span data-ttu-id="f7747-136">Określa URI pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="f7747-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="f7747-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f7747-137">-ForceRerun</span></span>
<span data-ttu-id="f7747-138">Wskazuje, że to polecenie cmdlet wymusza ponowne uruchomić tę samą konfigurację rozszerzenia na komputerze wirtualnym bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="f7747-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f7747-139">Wartość może być dowolnym ciągiem innym niż bieżąca wartość.</span><span class="sxs-lookup"><span data-stu-id="f7747-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="f7747-140">Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal stosuje aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="f7747-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f7747-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7747-141">-InputObject</span></span>
<span data-ttu-id="f7747-142">Obiekt rozszerzenia MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="f7747-142">VM extension object.</span></span>

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

### <span data-ttu-id="f7747-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f7747-143">-Location</span></span>
<span data-ttu-id="f7747-144">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7747-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f7747-145">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f7747-145">-Name</span></span>
<span data-ttu-id="f7747-146">Określa nazwę niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="f7747-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="f7747-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f7747-147">-NoWait</span></span>
<span data-ttu-id="f7747-148">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="f7747-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f7747-149">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="f7747-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f7747-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7747-150">-ResourceGroupName</span></span>
<span data-ttu-id="f7747-151">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7747-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f7747-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7747-152">-ResourceId</span></span>
<span data-ttu-id="f7747-153">Identyfikator zasobu rozszerzenia MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="f7747-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="f7747-154">- Uruchom</span><span class="sxs-lookup"><span data-stu-id="f7747-154">-Run</span></span>
<span data-ttu-id="f7747-155">Określa polecenie, które ma być uruchamiane przez skrypt.</span><span class="sxs-lookup"><span data-stu-id="f7747-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="f7747-156">- SecureExecution</span><span class="sxs-lookup"><span data-stu-id="f7747-156">-SecureExecution</span></span>
<span data-ttu-id="f7747-157">Wskazuje, że to polecenie cmdlet zapewnia, że wartość parametru *Uruchom* nie jest rejestrowana na serwerze ani zwracana użytkownikowi za pomocą interfejsu API rozszerzenia GET.</span><span class="sxs-lookup"><span data-stu-id="f7747-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="f7747-158">Wartość polecenia *Uruchom może zawierać* tajemnice lub hasła, które mają zostać bezpiecznie przekazane do pliku skryptu.</span><span class="sxs-lookup"><span data-stu-id="f7747-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="f7747-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f7747-159">-StorageAccountKey</span></span>
<span data-ttu-id="f7747-160">Określa klucz kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7747-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="f7747-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f7747-161">-StorageAccountName</span></span>
<span data-ttu-id="f7747-162">Określa nazwę konta magazynu platformy Azure, na którym to polecenie cmdlet przechowuje skrypt.</span><span class="sxs-lookup"><span data-stu-id="f7747-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="f7747-163">- StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f7747-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="f7747-164">Określa sufiks punktu końcowego magazynu.</span><span class="sxs-lookup"><span data-stu-id="f7747-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="f7747-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f7747-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="f7747-166">Określa wersję rozszerzenia do użycia dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7747-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="f7747-167">Aby uzyskać wersję, uruchom Get-AzVMExtensionImage cmdlet z wartością Microsoft.Compute dla parametru *PublisherName* i CustomScriptExtension dla *parametru Type.*</span><span class="sxs-lookup"><span data-stu-id="f7747-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="f7747-168">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="f7747-168">-VMName</span></span>
<span data-ttu-id="f7747-169">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7747-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f7747-170">To polecenie cmdlet dodaje rozszerzenie skryptu niestandardowego dla maszyny wirtualnej, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f7747-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7747-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="f7747-171">-VMObject</span></span>
<span data-ttu-id="f7747-172">Obiekt MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="f7747-172">VM object.</span></span>

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

### <span data-ttu-id="f7747-173">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7747-173">-Confirm</span></span>
<span data-ttu-id="f7747-174">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f7747-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7747-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7747-175">-WhatIf</span></span>
<span data-ttu-id="f7747-176">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7747-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7747-177">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f7747-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7747-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7747-178">CommonParameters</span></span>
<span data-ttu-id="f7747-179">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7747-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7747-180">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7747-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7747-181">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7747-181">INPUTS</span></span>

### <span data-ttu-id="f7747-182">System.String</span><span class="sxs-lookup"><span data-stu-id="f7747-182">System.String</span></span>

### <span data-ttu-id="f7747-183">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f7747-183">System.String[]</span></span>

### <span data-ttu-id="f7747-184">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="f7747-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7747-185">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7747-185">OUTPUTS</span></span>

### <span data-ttu-id="f7747-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f7747-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f7747-187">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f7747-187">NOTES</span></span>

## <span data-ttu-id="f7747-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7747-188">RELATED LINKS</span></span>

[<span data-ttu-id="f7747-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f7747-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="f7747-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f7747-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)



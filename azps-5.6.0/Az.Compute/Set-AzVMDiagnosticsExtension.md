---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9e33f3e956f7d1fee0d93eebf5e14fa0df460303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013690"
---
# <span data-ttu-id="71b8f-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="71b8f-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="71b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="71b8f-103">Konfiguruje rozszerzenie diagnostyki platformy Azure na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="71b8f-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="71b8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71b8f-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71b8f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="71b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="71b8f-106">Polecenie **cmdlet Set-AzVMDiagnosticsExtension** konfiguruje rozszerzenie diagnostyki platformy Azure na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="71b8f-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="71b8f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="71b8f-108">Przykład 1. Włączanie diagnostyki przy użyciu konta magazynu określonego w pliku konfiguracji diagnostyki</span><span class="sxs-lookup"><span data-stu-id="71b8f-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="71b8f-109">To polecenie używa pliku konfiguracji diagnostyki w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="71b8f-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="71b8f-110">Plik diagnostics_publicconfig.xml publiczną konfigurację języka XML dla rozszerzenia diagnostyki, w tym nazwę konta magazynu, do którego będą wysyłane dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="71b8f-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="71b8f-111">Konto magazynu diagnostycznego musi znajdować się w tej samej subskrypcji, co maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="71b8f-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="71b8f-112">Przykład 2. Włączanie diagnostyki przy użyciu nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="71b8f-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="71b8f-113">To polecenie używa nazwy konta magazynu w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="71b8f-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="71b8f-114">Jeśli konfiguracja diagnostyki nie określa nazwy konta magazynu lub chcesz zastąpić nazwę konta magazynu diagnostycznego określoną w pliku konfiguracji, użyj *parametru StorageAccountName.*</span><span class="sxs-lookup"><span data-stu-id="71b8f-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="71b8f-115">Konto magazynu diagnostycznego musi znajdować się w tej samej subskrypcji, co maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="71b8f-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="71b8f-116">Przykład 3. Włączanie diagnostyki przy użyciu nazwy i klucza konta magazynu</span><span class="sxs-lookup"><span data-stu-id="71b8f-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="71b8f-117">To polecenie używa nazwy konta magazynu i klucza w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="71b8f-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="71b8f-118">Jeśli konto magazynu diagnostycznego znajduje się w innej subskrypcji niż maszyny wirtualnej, włącz wysyłanie danych diagnostycznych do tego konta magazynu, jawnie określając jego nazwę i klucz.</span><span class="sxs-lookup"><span data-stu-id="71b8f-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="71b8f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71b8f-119">PARAMETERS</span></span>

### <span data-ttu-id="71b8f-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="71b8f-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="71b8f-121">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="71b8f-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b8f-122">-DefaultProfile</span></span>
<span data-ttu-id="71b8f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71b8f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71b8f-124">- DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="71b8f-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="71b8f-125">Określa ścieżkę pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="71b8f-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="71b8f-126">-Location</span></span>
<span data-ttu-id="71b8f-127">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="71b8f-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="71b8f-128">-Name</span></span>
<span data-ttu-id="71b8f-129">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="71b8f-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71b8f-130">-NoWait</span></span>
<span data-ttu-id="71b8f-131">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="71b8f-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="71b8f-132">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="71b8f-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="71b8f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b8f-133">-ResourceGroupName</span></span>
<span data-ttu-id="71b8f-134">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="71b8f-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="71b8f-135">- StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b8f-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="71b8f-136">Określa punkt końcowy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="71b8f-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="71b8f-137">-StorageAccountKey</span></span>
<span data-ttu-id="71b8f-138">Określa klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="71b8f-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="71b8f-139">-StorageAccountName</span></span>
<span data-ttu-id="71b8f-140">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="71b8f-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-141">- StorageContext</span><span class="sxs-lookup"><span data-stu-id="71b8f-141">-StorageContext</span></span>
<span data-ttu-id="71b8f-142">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71b8f-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="71b8f-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="71b8f-144">Określa wersję rozszerzenia do użycia dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="71b8f-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="71b8f-145">Aby uzyskać wersję, uruchom Get-AzVMExtensionImage cmdlet z wartością Microsoft.Compute dla parametru *PublisherName* i VMAccessAgent dla *parametru Type.*</span><span class="sxs-lookup"><span data-stu-id="71b8f-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b8f-146">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="71b8f-146">-VMName</span></span>
<span data-ttu-id="71b8f-147">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71b8f-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="71b8f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b8f-148">CommonParameters</span></span>
<span data-ttu-id="71b8f-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b8f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b8f-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71b8f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b8f-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71b8f-151">INPUTS</span></span>

### <span data-ttu-id="71b8f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="71b8f-152">System.String</span></span>

### <span data-ttu-id="71b8f-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="71b8f-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="71b8f-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71b8f-154">System.Boolean</span></span>

## <span data-ttu-id="71b8f-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71b8f-155">OUTPUTS</span></span>

### <span data-ttu-id="71b8f-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="71b8f-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="71b8f-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71b8f-157">NOTES</span></span>

## <span data-ttu-id="71b8f-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71b8f-158">RELATED LINKS</span></span>

[<span data-ttu-id="71b8f-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="71b8f-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="71b8f-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="71b8f-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="71b8f-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="71b8f-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)



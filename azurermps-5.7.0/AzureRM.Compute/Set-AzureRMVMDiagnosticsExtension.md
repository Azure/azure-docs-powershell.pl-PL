---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: d93fd01fb178f093b6ed5527cca0c018cebe4f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548179"
---
# <span data-ttu-id="dda93-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dda93-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="dda93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dda93-102">SYNOPSIS</span></span>
<span data-ttu-id="dda93-103">Konfiguruje rozszerzenie Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dda93-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dda93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dda93-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [<CommonParameters>]
```

## <span data-ttu-id="dda93-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dda93-105">DESCRIPTION</span></span>
<span data-ttu-id="dda93-106">Polecenie cmdlet **Set-AzureRmVMDiagnosticsExtension** konfiguruje rozszerzenie Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dda93-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="dda93-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dda93-107">EXAMPLES</span></span>

### <span data-ttu-id="dda93-108">Przykład 1: Włączanie diagnostyki przy użyciu konta magazynu określonego w pliku konfiguracji diagnostyki</span><span class="sxs-lookup"><span data-stu-id="dda93-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="dda93-109">To polecenie używa pliku konfiguracji diagnostyki w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="dda93-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="dda93-110">Plik diagnostics_publicconfig.xml zawiera publiczną konfigurację XML rozszerzenia diagnostycznego, w tym nazwę konta magazynu, na które zostaną wysłane dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="dda93-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="dda93-111">Konto magazynu diagnostycznego musi znajdować się w tej samej subskrypcji co maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="dda93-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="dda93-112">Przykład 2: Włączanie diagnostyki przy użyciu nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="dda93-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="dda93-113">W tym poleceniu jest używana nazwa konta magazynu w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="dda93-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="dda93-114">Jeśli konfiguracja diagnostyki nie określa nazwy konta magazynu lub jeśli chcesz zastąpić nazwę konta magazynu diagnostycznego określoną w pliku konfiguracji, użyj parametru *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="dda93-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="dda93-115">Konto magazynu diagnostycznego musi znajdować się w tej samej subskrypcji co maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="dda93-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="dda93-116">Przykład 3: Włączanie diagnostyki przy użyciu nazwy i klucza konta magazynu</span><span class="sxs-lookup"><span data-stu-id="dda93-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="dda93-117">W tym poleceniu jest używana nazwa i klucz konta magazynu w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="dda93-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="dda93-118">Jeśli konto magazynu diagnostycznego jest w innej subskrypcji niż maszyna wirtualna, Włącz wysyłanie danych diagnostycznych do tego konta magazynu, jawnie określając jego nazwę i klucz.</span><span class="sxs-lookup"><span data-stu-id="dda93-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="dda93-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dda93-119">PARAMETERS</span></span>

### <span data-ttu-id="dda93-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dda93-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="dda93-121">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="dda93-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="dda93-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="dda93-123">Określa ścieżkę pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dda93-123">Specifies the path of the configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dda93-124">-Location</span></span>
<span data-ttu-id="dda93-125">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dda93-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dda93-126">-Name</span></span>
<span data-ttu-id="dda93-127">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="dda93-127">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda93-128">-ResourceGroupName</span></span>
<span data-ttu-id="dda93-129">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dda93-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dda93-130">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="dda93-130">-StorageAccountEndpoint</span></span>
<span data-ttu-id="dda93-131">Określa punkt końcowy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dda93-131">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dda93-132">-StorageAccountKey</span></span>
<span data-ttu-id="dda93-133">Określa klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dda93-133">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dda93-134">-StorageAccountName</span></span>
<span data-ttu-id="dda93-135">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="dda93-135">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-136">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dda93-136">-StorageContext</span></span>
<span data-ttu-id="dda93-137">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="dda93-137">Specifies the Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dda93-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="dda93-139">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dda93-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="dda93-140">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzureRmVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="dda93-140">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda93-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="dda93-141">-VMName</span></span>
<span data-ttu-id="dda93-142">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda93-142">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dda93-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda93-143">CommonParameters</span></span>
<span data-ttu-id="dda93-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda93-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda93-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda93-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda93-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dda93-146">INPUTS</span></span>

### <span data-ttu-id="dda93-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dda93-147">None</span></span>
<span data-ttu-id="dda93-148">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dda93-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dda93-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dda93-149">OUTPUTS</span></span>

## <span data-ttu-id="dda93-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dda93-150">NOTES</span></span>

## <span data-ttu-id="dda93-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dda93-151">RELATED LINKS</span></span>

[<span data-ttu-id="dda93-152">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dda93-152">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="dda93-153">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="dda93-153">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="dda93-154">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="dda93-154">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9626198c9a512ef65a2011b040378f194abd50ef
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893373"
---
# <span data-ttu-id="b6568-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b6568-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="b6568-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6568-102">SYNOPSIS</span></span>
<span data-ttu-id="b6568-103">Konfiguruje rozszerzenie Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6568-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="b6568-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6568-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6568-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6568-105">DESCRIPTION</span></span>
<span data-ttu-id="b6568-106">Polecenie cmdlet **Set-AzVMDiagnosticsExtension** konfiguruje rozszerzenie Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6568-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="b6568-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6568-107">EXAMPLES</span></span>

### <span data-ttu-id="b6568-108">Przykład 1: Włączanie diagnostyki przy użyciu konta magazynu określonego w pliku konfiguracji diagnostyki</span><span class="sxs-lookup"><span data-stu-id="b6568-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="b6568-109">To polecenie używa pliku konfiguracji diagnostyki w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="b6568-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="b6568-110">Plik diagnostics_publicconfig.xml zawiera publiczną konfigurację XML rozszerzenia diagnostycznego, w tym nazwę konta magazynu, na które zostaną wysłane dane diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="b6568-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="b6568-111">Konto magazynu diagnostycznego musi znajdować się w tej samej subskrypcji co maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="b6568-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="b6568-112">Przykład 2: Włączanie diagnostyki przy użyciu nazwy konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b6568-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="b6568-113">W tym poleceniu jest używana nazwa konta magazynu w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="b6568-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="b6568-114">Jeśli konfiguracja diagnostyki nie określa nazwy konta magazynu lub jeśli chcesz zastąpić nazwę konta magazynu diagnostycznego określoną w pliku konfiguracji, użyj parametru *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="b6568-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="b6568-115">Konto magazynu diagnostycznego musi znajdować się w tej samej subskrypcji co maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="b6568-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="b6568-116">Przykład 3: Włączanie diagnostyki przy użyciu nazwy i klucza konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b6568-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="b6568-117">W tym poleceniu jest używana nazwa i klucz konta magazynu w celu włączenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="b6568-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="b6568-118">Jeśli konto magazynu diagnostycznego jest w innej subskrypcji niż maszyna wirtualna, Włącz wysyłanie danych diagnostycznych do tego konta magazynu, jawnie określając jego nazwę i klucz.</span><span class="sxs-lookup"><span data-stu-id="b6568-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="b6568-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6568-119">PARAMETERS</span></span>

### <span data-ttu-id="b6568-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b6568-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b6568-121">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="b6568-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="b6568-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6568-122">-DefaultProfile</span></span>
<span data-ttu-id="b6568-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6568-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6568-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="b6568-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="b6568-125">Określa ścieżkę pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="b6568-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="b6568-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b6568-126">-Location</span></span>
<span data-ttu-id="b6568-127">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6568-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="b6568-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6568-128">-Name</span></span>
<span data-ttu-id="b6568-129">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b6568-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="b6568-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6568-130">-ResourceGroupName</span></span>
<span data-ttu-id="b6568-131">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6568-131">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b6568-132">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6568-132">-StorageAccountEndpoint</span></span>
<span data-ttu-id="b6568-133">Określa punkt końcowy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b6568-133">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="b6568-134">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b6568-134">-StorageAccountKey</span></span>
<span data-ttu-id="b6568-135">Określa klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b6568-135">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="b6568-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b6568-136">-StorageAccountName</span></span>
<span data-ttu-id="b6568-137">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b6568-137">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="b6568-138">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b6568-138">-StorageContext</span></span>
<span data-ttu-id="b6568-139">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b6568-139">Specifies the Azure storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6568-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b6568-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="b6568-141">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6568-141">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="b6568-142">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="b6568-142">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="b6568-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="b6568-143">-VMName</span></span>
<span data-ttu-id="b6568-144">Określa nazwę maszyny wirtualnej, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6568-144">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b6568-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6568-145">CommonParameters</span></span>
<span data-ttu-id="b6568-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6568-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6568-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6568-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6568-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6568-148">INPUTS</span></span>

### <span data-ttu-id="b6568-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b6568-149">None</span></span>
<span data-ttu-id="b6568-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b6568-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6568-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6568-151">OUTPUTS</span></span>

### <span data-ttu-id="b6568-152">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b6568-152">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b6568-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6568-153">NOTES</span></span>

## <span data-ttu-id="b6568-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6568-154">RELATED LINKS</span></span>

[<span data-ttu-id="b6568-155">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b6568-155">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="b6568-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b6568-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="b6568-157">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b6568-157">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504114"
---
# <span data-ttu-id="1f031-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1f031-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="1f031-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f031-102">SYNOPSIS</span></span>
<span data-ttu-id="1f031-103">Pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f031-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="1f031-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f031-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f031-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f031-105">DESCRIPTION</span></span>
<span data-ttu-id="1f031-106">Polecenie cmdlet **Get-AzVMExtensionImage** pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1f031-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="1f031-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f031-107">EXAMPLES</span></span>

### <span data-ttu-id="1f031-108">Przykład 1: uzyskiwanie wersji obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="1f031-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="1f031-109">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy i typu.</span><span class="sxs-lookup"><span data-stu-id="1f031-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="1f031-110">Przykład 2: pobieranie wersji obrazu rozszerzenia z funkcją filtrowania w wersji</span><span class="sxs-lookup"><span data-stu-id="1f031-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="1f031-111">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy, typu i wersji, rozpoczynając od 12.</span><span class="sxs-lookup"><span data-stu-id="1f031-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="1f031-112">Przykład 3: pobieranie wersji obrazu rozszerzenia z funkcją filtrowania w wersji</span><span class="sxs-lookup"><span data-stu-id="1f031-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="1f031-113">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy, typu i wersji.</span><span class="sxs-lookup"><span data-stu-id="1f031-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="1f031-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f031-114">PARAMETERS</span></span>

### <span data-ttu-id="1f031-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f031-115">-DefaultProfile</span></span>
<span data-ttu-id="1f031-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f031-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f031-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="1f031-117">-FilterExpression</span></span>
<span data-ttu-id="1f031-118">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="1f031-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f031-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1f031-119">-Location</span></span>
<span data-ttu-id="1f031-120">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1f031-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="1f031-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="1f031-121">-PublisherName</span></span>
<span data-ttu-id="1f031-122">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1f031-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="1f031-123">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="1f031-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="1f031-124">-Type</span><span class="sxs-lookup"><span data-stu-id="1f031-124">-Type</span></span>
<span data-ttu-id="1f031-125">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1f031-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="1f031-126">Aby uzyskać typ rozszerzenia, użyj polecenia cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="1f031-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="1f031-127">-Version</span><span class="sxs-lookup"><span data-stu-id="1f031-127">-Version</span></span>
<span data-ttu-id="1f031-128">Określa wersję rozszerzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f031-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1f031-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f031-129">CommonParameters</span></span>
<span data-ttu-id="1f031-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f031-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f031-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f031-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f031-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f031-132">INPUTS</span></span>

### <span data-ttu-id="1f031-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f031-133">System.String</span></span>

## <span data-ttu-id="1f031-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f031-134">OUTPUTS</span></span>

### <span data-ttu-id="1f031-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1f031-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="1f031-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="1f031-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="1f031-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f031-137">NOTES</span></span>

## <span data-ttu-id="1f031-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f031-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f031-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="1f031-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="1f031-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1f031-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="1f031-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1f031-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318084"
---
# <span data-ttu-id="11d79-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="11d79-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="11d79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11d79-102">SYNOPSIS</span></span>
<span data-ttu-id="11d79-103">Pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11d79-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="11d79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11d79-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11d79-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11d79-105">DESCRIPTION</span></span>
<span data-ttu-id="11d79-106">Polecenie cmdlet **Get-AzVMExtensionImage** pobiera wszystkie wersje rozszerzenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11d79-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="11d79-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11d79-107">EXAMPLES</span></span>

### <span data-ttu-id="11d79-108">Przykład 1: uzyskiwanie wersji obrazu rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="11d79-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="11d79-109">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy i typu.</span><span class="sxs-lookup"><span data-stu-id="11d79-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="11d79-110">Przykład 2: pobieranie wersji obrazu rozszerzenia z funkcją filtrowania w wersji</span><span class="sxs-lookup"><span data-stu-id="11d79-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="11d79-111">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy, typu i wersji, rozpoczynając od 12.</span><span class="sxs-lookup"><span data-stu-id="11d79-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="11d79-112">Przykład 3: pobieranie wersji obrazu rozszerzenia z funkcją filtrowania w wersji</span><span class="sxs-lookup"><span data-stu-id="11d79-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="11d79-113">To polecenie pobiera wszystkie wersje obrazu rozszerzenia dla określonej lokalizacji, wydawcy, typu i wersji.</span><span class="sxs-lookup"><span data-stu-id="11d79-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="11d79-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11d79-114">PARAMETERS</span></span>

### <span data-ttu-id="11d79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d79-115">-DefaultProfile</span></span>
<span data-ttu-id="11d79-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11d79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11d79-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="11d79-117">-FilterExpression</span></span>
<span data-ttu-id="11d79-118">Określa wyrażenie filtru.</span><span class="sxs-lookup"><span data-stu-id="11d79-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="11d79-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="11d79-119">-Location</span></span>
<span data-ttu-id="11d79-120">Określa lokalizację rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="11d79-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="11d79-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="11d79-121">-PublisherName</span></span>
<span data-ttu-id="11d79-122">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="11d79-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="11d79-123">Aby uzyskać wydawcę rozszerzenia, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="11d79-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="11d79-124">-Type</span><span class="sxs-lookup"><span data-stu-id="11d79-124">-Type</span></span>
<span data-ttu-id="11d79-125">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="11d79-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="11d79-126">Aby uzyskać typ rozszerzenia, użyj polecenia cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="11d79-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="11d79-127">-Version</span><span class="sxs-lookup"><span data-stu-id="11d79-127">-Version</span></span>
<span data-ttu-id="11d79-128">Określa wersję rozszerzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11d79-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="11d79-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d79-129">CommonParameters</span></span>
<span data-ttu-id="11d79-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d79-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d79-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11d79-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d79-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11d79-132">INPUTS</span></span>

### <span data-ttu-id="11d79-133">System. String</span><span class="sxs-lookup"><span data-stu-id="11d79-133">System.String</span></span>

## <span data-ttu-id="11d79-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11d79-134">OUTPUTS</span></span>

### <span data-ttu-id="11d79-135">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="11d79-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="11d79-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="11d79-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="11d79-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11d79-137">NOTES</span></span>

## <span data-ttu-id="11d79-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11d79-138">RELATED LINKS</span></span>

[<span data-ttu-id="11d79-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="11d79-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="11d79-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="11d79-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="11d79-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="11d79-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)



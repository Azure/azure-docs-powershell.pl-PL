---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 33446cf9e14175c67e3f2fd2fa5dead33b88f526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181698"
---
# <span data-ttu-id="21f92-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="21f92-101">Get-AzVMImage</span></span>

## <span data-ttu-id="21f92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f92-102">SYNOPSIS</span></span>
<span data-ttu-id="21f92-103">Pobiera wszystkie wersje maszyny WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="21f92-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="21f92-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21f92-104">SYNTAX</span></span>

### <span data-ttu-id="21f92-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="21f92-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21f92-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="21f92-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21f92-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="21f92-107">DESCRIPTION</span></span>
<span data-ttu-id="21f92-108">Polecenie **cmdlet Get-AzVMImage** pobiera wszystkie wersje maszyny WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="21f92-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="21f92-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21f92-109">EXAMPLES</span></span>

### <span data-ttu-id="21f92-110">Przykład 1. Uzyskiwanie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="21f92-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="21f92-111">To polecenie pobiera wszystkie wersje maszyny WIRTUALNEJ zgodne z określonymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="21f92-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="21f92-112">Przykład 2. Uzyskiwanie obiektu VMImage</span><span class="sxs-lookup"><span data-stu-id="21f92-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="21f92-113">To polecenie pobiera określoną wersję maszyny WIRTUALNEJ, która odpowiada określonym wartościom.</span><span class="sxs-lookup"><span data-stu-id="21f92-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="21f92-114">Przykład 3. Uzyskiwanie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="21f92-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="21f92-115">To polecenie pobiera wszystkie wersje maszyny WIRTUALNEJ zgodne z określonymi wartościami za pomocą filtrowania w określonej wersji.</span><span class="sxs-lookup"><span data-stu-id="21f92-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="21f92-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21f92-116">PARAMETERS</span></span>

### <span data-ttu-id="21f92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f92-117">-DefaultProfile</span></span>
<span data-ttu-id="21f92-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21f92-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21f92-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="21f92-119">-Location</span></span>
<span data-ttu-id="21f92-120">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21f92-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="21f92-121">— Oferta</span><span class="sxs-lookup"><span data-stu-id="21f92-121">-Offer</span></span>
<span data-ttu-id="21f92-122">Określa typ oferty maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21f92-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="21f92-123">Aby uzyskać ofertę obrazu, użyj Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f92-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="21f92-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="21f92-124">-OrderBy</span></span>
<span data-ttu-id="21f92-125">Określa kolejność zwracanych wyników.</span><span class="sxs-lookup"><span data-stu-id="21f92-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="21f92-126">Sformatowane jako zapytanie OData.</span><span class="sxs-lookup"><span data-stu-id="21f92-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f92-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="21f92-127">-PublisherName</span></span>
<span data-ttu-id="21f92-128">Określa wydawcę obrazów MASZYNY WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="21f92-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="21f92-129">Aby uzyskać wydawcę obrazu, użyj Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f92-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="21f92-130">— jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="21f92-130">-Skus</span></span>
<span data-ttu-id="21f92-131">Określa sKU MASZYNY.WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="21f92-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="21f92-132">Aby uzyskać sKU, użyj polecenia cmdlet Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21f92-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="21f92-133">— Na górze</span><span class="sxs-lookup"><span data-stu-id="21f92-133">-Top</span></span>
<span data-ttu-id="21f92-134">Określa maksymalną liczbę zwracanych obrazów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="21f92-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f92-135">— Wersja</span><span class="sxs-lookup"><span data-stu-id="21f92-135">-Version</span></span>
<span data-ttu-id="21f92-136">Określa wersję programu VMImage.</span><span class="sxs-lookup"><span data-stu-id="21f92-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f92-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f92-137">CommonParameters</span></span>
<span data-ttu-id="21f92-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f92-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f92-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21f92-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f92-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21f92-140">INPUTS</span></span>

### <span data-ttu-id="21f92-141">System.String</span><span class="sxs-lookup"><span data-stu-id="21f92-141">System.String</span></span>

## <span data-ttu-id="21f92-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21f92-142">OUTPUTS</span></span>

### <span data-ttu-id="21f92-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="21f92-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="21f92-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="21f92-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="21f92-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21f92-145">NOTES</span></span>

## <span data-ttu-id="21f92-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21f92-146">RELATED LINKS</span></span>

[<span data-ttu-id="21f92-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="21f92-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="21f92-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="21f92-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="21f92-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="21f92-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="21f92-150">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="21f92-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



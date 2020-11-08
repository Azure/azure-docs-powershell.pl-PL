---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 350e03d6e238eb0cf1aa6b27da6b9a321603a664
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062603"
---
# <span data-ttu-id="9b0ff-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9b0ff-101">Get-AzVMImage</span></span>

## <span data-ttu-id="9b0ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0ff-103">Pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9b0ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b0ff-104">SYNTAX</span></span>

### <span data-ttu-id="9b0ff-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="9b0ff-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b0ff-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="9b0ff-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b0ff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9b0ff-107">DESCRIPTION</span></span>
<span data-ttu-id="9b0ff-108">Polecenie cmdlet **Get-AzVMImage** pobiera wszystkie wersje VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9b0ff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b0ff-109">EXAMPLES</span></span>

### <span data-ttu-id="9b0ff-110">Przykład 1: pobieranie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="9b0ff-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="9b0ff-111">To polecenie pobiera wszystkie wersje VMImage, które pasują do określonych wartości.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="9b0ff-112">Przykład 2: Pobieranie obiektu VMImage</span><span class="sxs-lookup"><span data-stu-id="9b0ff-112">Example 2: Get VMImage object</span></span>
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
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="9b0ff-113">To polecenie pobiera określoną wersję programu VMImage zgodną z określonymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="9b0ff-114">Przykład 3: pobieranie obiektów VMImage</span><span class="sxs-lookup"><span data-stu-id="9b0ff-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="9b0ff-115">To polecenie pobiera wszystkie wersje VMImage, które pasują do określonych wartości za pomocą filtrowania w wersji.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="9b0ff-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b0ff-116">PARAMETERS</span></span>

### <span data-ttu-id="9b0ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0ff-117">-DefaultProfile</span></span>
<span data-ttu-id="9b0ff-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b0ff-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9b0ff-119">-Location</span></span>
<span data-ttu-id="9b0ff-120">Określa lokalizację VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="9b0ff-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="9b0ff-121">-Offer</span></span>
<span data-ttu-id="9b0ff-122">Określa typ oferty VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9b0ff-123">Aby uzyskać ofertę obrazu, użyj polecenia cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9b0ff-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9b0ff-124">-OrderBy</span></span>
<span data-ttu-id="9b0ff-125">Określa kolejność zwróconych wyników.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="9b0ff-126">Sformatowana jako kwerenda OData.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-126">Formatted as an OData query.</span></span>

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

### <span data-ttu-id="9b0ff-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9b0ff-127">-PublisherName</span></span>
<span data-ttu-id="9b0ff-128">Umożliwia określenie wydawcy VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="9b0ff-129">Aby uzyskać wydawcę obrazu, użyj polecenia cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9b0ff-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="9b0ff-130">-Skus</span></span>
<span data-ttu-id="9b0ff-131">Określa VMImage SKU.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9b0ff-132">Aby uzyskać jednostkę SKU, użyj polecenia cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9b0ff-133">-Początek</span><span class="sxs-lookup"><span data-stu-id="9b0ff-133">-Top</span></span>
<span data-ttu-id="9b0ff-134">Określa maksymalną liczbę zwracanych obrazów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-134">Specifies the maximum number of virtual machine images returned.</span></span> 

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

### <span data-ttu-id="9b0ff-135">-Version</span><span class="sxs-lookup"><span data-stu-id="9b0ff-135">-Version</span></span>
<span data-ttu-id="9b0ff-136">Określa wersję VMImage.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-136">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="9b0ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0ff-137">CommonParameters</span></span>
<span data-ttu-id="9b0ff-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b0ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0ff-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b0ff-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0ff-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b0ff-140">INPUTS</span></span>

### <span data-ttu-id="9b0ff-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9b0ff-141">System.String</span></span>

## <span data-ttu-id="9b0ff-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b0ff-142">OUTPUTS</span></span>

### <span data-ttu-id="9b0ff-143">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="9b0ff-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="9b0ff-144">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="9b0ff-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="9b0ff-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b0ff-145">NOTES</span></span>

## <span data-ttu-id="9b0ff-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b0ff-146">RELATED LINKS</span></span>

[<span data-ttu-id="9b0ff-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9b0ff-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9b0ff-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9b0ff-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9b0ff-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9b0ff-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9b0ff-150">Zapisz — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9b0ff-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



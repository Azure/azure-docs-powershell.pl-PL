---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193563"
---
# <span data-ttu-id="11782-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="11782-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="11782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11782-102">SYNOPSIS</span></span>
<span data-ttu-id="11782-103">Zdefiniuj dla zasobu sku Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="11782-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="11782-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11782-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11782-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11782-105">DESCRIPTION</span></span>
<span data-ttu-id="11782-106">Polecenie New-AzVirtualApplianceSkuProperties definiuje sku dla zasobu Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="11782-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="11782-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11782-107">EXAMPLES</span></span>

### <span data-ttu-id="11782-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11782-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="11782-109">Utwórz obiekt Właściwości SKU urządzenia wirtualnego, który będzie używany z New-AzNetworkVirtualAppliance urządzeniem.</span><span class="sxs-lookup"><span data-stu-id="11782-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="11782-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11782-110">PARAMETERS</span></span>

### <span data-ttu-id="11782-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="11782-111">-BundledScaleUnit</span></span>
<span data-ttu-id="11782-112">Jednostka skalowania w pakiecie.</span><span class="sxs-lookup"><span data-stu-id="11782-112">The bundled scale unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11782-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11782-113">-DefaultProfile</span></span>
<span data-ttu-id="11782-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11782-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11782-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="11782-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="11782-116">Wersja market place.</span><span class="sxs-lookup"><span data-stu-id="11782-116">The market place version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11782-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="11782-117">-VendorName</span></span>
<span data-ttu-id="11782-118">Nazwa dostawcy.</span><span class="sxs-lookup"><span data-stu-id="11782-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11782-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11782-119">CommonParameters</span></span>
<span data-ttu-id="11782-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11782-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11782-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11782-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11782-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11782-122">INPUTS</span></span>

### <span data-ttu-id="11782-123">Brak</span><span class="sxs-lookup"><span data-stu-id="11782-123">None</span></span>

## <span data-ttu-id="11782-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11782-124">OUTPUTS</span></span>

### <span data-ttu-id="11782-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="11782-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="11782-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11782-126">NOTES</span></span>

## <span data-ttu-id="11782-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11782-127">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006177"
---
# <span data-ttu-id="13e58-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="13e58-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="13e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13e58-102">SYNOPSIS</span></span>
<span data-ttu-id="13e58-103">Definiowanie zasobu w środowisku SKU Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="13e58-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="13e58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13e58-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13e58-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="13e58-105">DESCRIPTION</span></span>
<span data-ttu-id="13e58-106">Polecenie New-AzVirtualApplianceSkuProperties definiuje sku dla zasobu Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="13e58-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="13e58-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13e58-107">EXAMPLES</span></span>

### <span data-ttu-id="13e58-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13e58-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="13e58-109">Utwórz obiekt Właściwości SKU urządzenia wirtualnego, który będzie używany z New-AzNetworkVirtualAppliance urządzeniem.</span><span class="sxs-lookup"><span data-stu-id="13e58-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="13e58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13e58-110">PARAMETERS</span></span>

### <span data-ttu-id="13e58-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="13e58-111">-BundledScaleUnit</span></span>
<span data-ttu-id="13e58-112">Jednostka skalowania w pakiecie.</span><span class="sxs-lookup"><span data-stu-id="13e58-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="13e58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e58-113">-DefaultProfile</span></span>
<span data-ttu-id="13e58-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13e58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e58-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="13e58-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="13e58-116">Wersja market place.</span><span class="sxs-lookup"><span data-stu-id="13e58-116">The market place version.</span></span>

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

### <span data-ttu-id="13e58-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="13e58-117">-VendorName</span></span>
<span data-ttu-id="13e58-118">Nazwa dostawcy.</span><span class="sxs-lookup"><span data-stu-id="13e58-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="13e58-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e58-119">CommonParameters</span></span>
<span data-ttu-id="13e58-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13e58-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e58-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13e58-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e58-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13e58-122">INPUTS</span></span>

### <span data-ttu-id="13e58-123">Brak</span><span class="sxs-lookup"><span data-stu-id="13e58-123">None</span></span>

## <span data-ttu-id="13e58-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13e58-124">OUTPUTS</span></span>

### <span data-ttu-id="13e58-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="13e58-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="13e58-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13e58-126">NOTES</span></span>

## <span data-ttu-id="13e58-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13e58-127">RELATED LINKS</span></span>

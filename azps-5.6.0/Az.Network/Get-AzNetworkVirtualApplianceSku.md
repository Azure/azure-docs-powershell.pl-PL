---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e165b481b1321f5ddd81766452120f55f6f0e153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954529"
---
# <span data-ttu-id="3634a-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="3634a-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="3634a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3634a-102">SYNOPSIS</span></span>
<span data-ttu-id="3634a-103">Pobierz lub na liście dostępne jednostki SKU wirtualnego urządzenia sieciowego w spisie.</span><span class="sxs-lookup"><span data-stu-id="3634a-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="3634a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3634a-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3634a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3634a-105">DESCRIPTION</span></span>
<span data-ttu-id="3634a-106">Ten Get-AzNetworkVirtualApplianceSku pobiera lub wyświetla dostępne jednostki SKU wirtualnego urządzenia sieciowego w spisie produktów platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3634a-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="3634a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3634a-107">EXAMPLES</span></span>

### <span data-ttu-id="3634a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3634a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="3634a-109">Pobierz sku według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3634a-109">Get a sku by name.</span></span>

### <span data-ttu-id="3634a-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3634a-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="3634a-111">Lista wszystkich dostępnych jednostki SKU urządzenia wirtualnego sieci.</span><span class="sxs-lookup"><span data-stu-id="3634a-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="3634a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3634a-112">PARAMETERS</span></span>

### <span data-ttu-id="3634a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3634a-113">-DefaultProfile</span></span>
<span data-ttu-id="3634a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3634a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3634a-115">-SKUName</span><span class="sxs-lookup"><span data-stu-id="3634a-115">-SkuName</span></span>
<span data-ttu-id="3634a-116">Nazwa sku.</span><span class="sxs-lookup"><span data-stu-id="3634a-116">The Sku name.</span></span>

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

### <span data-ttu-id="3634a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3634a-117">CommonParameters</span></span>
<span data-ttu-id="3634a-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3634a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3634a-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3634a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3634a-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3634a-120">INPUTS</span></span>

### <span data-ttu-id="3634a-121">Brak</span><span class="sxs-lookup"><span data-stu-id="3634a-121">None</span></span>

## <span data-ttu-id="3634a-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3634a-122">OUTPUTS</span></span>

### <span data-ttu-id="3634a-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="3634a-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="3634a-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3634a-124">NOTES</span></span>

## <span data-ttu-id="3634a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3634a-125">RELATED LINKS</span></span>

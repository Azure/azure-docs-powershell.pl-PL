---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: a5febccec0ed09cde866925ce03d7025408b27f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552456"
---
# <span data-ttu-id="89e55-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="89e55-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="89e55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89e55-102">SYNOPSIS</span></span>
<span data-ttu-id="89e55-103">Tworzy wystąpienie PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="89e55-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89e55-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89e55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89e55-105">DESCRIPTION</span></span>
<span data-ttu-id="89e55-106">Polecenie pomocnika tworzenia wystąpienia PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="89e55-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="89e55-107">To polecenie jest używane z poleceniem New-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="89e55-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="89e55-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89e55-108">EXAMPLES</span></span>

### <span data-ttu-id="89e55-109">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="89e55-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="89e55-110">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="89e55-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="89e55-111">Tworzy usługę ApiManagement z VpnType zewnętrznych w regionie zachodnim Stanów Zjednoczonych z dodatkowym regionem w centrum centralnym.</span><span class="sxs-lookup"><span data-stu-id="89e55-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="89e55-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89e55-112">PARAMETERS</span></span>

### <span data-ttu-id="89e55-113">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="89e55-113">-Capacity</span></span>
<span data-ttu-id="89e55-114">Pojemność jednostki SKU usługi zarządzania interfejsem Azure API — dodatkowy region.</span><span class="sxs-lookup"><span data-stu-id="89e55-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="89e55-115">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="89e55-115">Default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e55-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="89e55-116">-Location</span></span>
<span data-ttu-id="89e55-117">Lokalizacja dodatkowego regionu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="89e55-117">Location of the additional deployment region.</span></span>

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

### <span data-ttu-id="89e55-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="89e55-118">-VirtualNetwork</span></span>
<span data-ttu-id="89e55-119">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania usługą Azure API.</span><span class="sxs-lookup"><span data-stu-id="89e55-119">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="89e55-120">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="89e55-120">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e55-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e55-121">-DefaultProfile</span></span>
<span data-ttu-id="89e55-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89e55-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e55-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e55-123">CommonParameters</span></span>
<span data-ttu-id="89e55-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e55-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e55-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e55-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e55-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89e55-126">INPUTS</span></span>

## <span data-ttu-id="89e55-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89e55-127">OUTPUTS</span></span>

### <span data-ttu-id="89e55-128">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="89e55-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="89e55-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89e55-129">NOTES</span></span>

## <span data-ttu-id="89e55-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89e55-130">RELATED LINKS</span></span>


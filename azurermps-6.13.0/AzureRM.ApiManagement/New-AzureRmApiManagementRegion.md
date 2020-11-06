---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8d292f6e03661ae55a63686a0282ce65292087f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526398"
---
# <span data-ttu-id="48248-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="48248-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="48248-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48248-102">SYNOPSIS</span></span>
<span data-ttu-id="48248-103">Tworzy wystąpienie PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="48248-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48248-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48248-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48248-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48248-105">DESCRIPTION</span></span>
<span data-ttu-id="48248-106">Polecenie pomocnika tworzenia wystąpienia PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="48248-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="48248-107">To polecenie jest używane z poleceniem New-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="48248-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="48248-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48248-108">EXAMPLES</span></span>

### <span data-ttu-id="48248-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48248-109">Example 1</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="48248-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="48248-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="48248-111">Tworzy usługę ApiManagement z VpnType zewnętrznych w regionie zachodnim Stanów Zjednoczonych z dodatkowym regionem w centrum centralnym.</span><span class="sxs-lookup"><span data-stu-id="48248-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="48248-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48248-112">PARAMETERS</span></span>

### <span data-ttu-id="48248-113">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="48248-113">-Capacity</span></span>
<span data-ttu-id="48248-114">Pojemność jednostki SKU usługi zarządzania interfejsem Azure API — dodatkowy region.</span><span class="sxs-lookup"><span data-stu-id="48248-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="48248-115">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="48248-115">Default value is 1.</span></span>

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

### <span data-ttu-id="48248-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48248-116">-DefaultProfile</span></span>
<span data-ttu-id="48248-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48248-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48248-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="48248-118">-Location</span></span>
<span data-ttu-id="48248-119">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="48248-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="48248-120">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="48248-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="48248-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48248-121">-VirtualNetwork</span></span>
<span data-ttu-id="48248-122">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania usługą Azure API.</span><span class="sxs-lookup"><span data-stu-id="48248-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="48248-123">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="48248-123">Default value is $null.</span></span>

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

### <span data-ttu-id="48248-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48248-124">CommonParameters</span></span>
<span data-ttu-id="48248-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48248-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48248-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48248-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48248-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48248-127">INPUTS</span></span>

### <span data-ttu-id="48248-128">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48248-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="48248-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48248-129">OUTPUTS</span></span>

### <span data-ttu-id="48248-130">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="48248-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="48248-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48248-131">NOTES</span></span>

## <span data-ttu-id="48248-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48248-132">RELATED LINKS</span></span>

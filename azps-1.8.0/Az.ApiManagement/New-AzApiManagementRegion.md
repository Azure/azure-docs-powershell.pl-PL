---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 13a6478f6124a6c7e017854918abfdf8b07165f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869491"
---
# <span data-ttu-id="04ef1-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="04ef1-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="04ef1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="04ef1-103">Tworzy wystąpienie PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="04ef1-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="04ef1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04ef1-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04ef1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="04ef1-106">Polecenie pomocnika tworzenia wystąpienia PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="04ef1-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="04ef1-107">To polecenie jest używane z poleceniem New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="04ef1-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="04ef1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04ef1-108">EXAMPLES</span></span>

### <span data-ttu-id="04ef1-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04ef1-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="04ef1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="04ef1-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="04ef1-111">Tworzy usługę ApiManagement z VpnType zewnętrznych w regionie zachodnim Stanów Zjednoczonych z dodatkowym regionem w centrum centralnym.</span><span class="sxs-lookup"><span data-stu-id="04ef1-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="04ef1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04ef1-112">PARAMETERS</span></span>

### <span data-ttu-id="04ef1-113">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="04ef1-113">-Capacity</span></span>
<span data-ttu-id="04ef1-114">Pojemność jednostki SKU usługi zarządzania interfejsem Azure API — dodatkowy region.</span><span class="sxs-lookup"><span data-stu-id="04ef1-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="04ef1-115">Wartość domyślna to 1.</span><span class="sxs-lookup"><span data-stu-id="04ef1-115">Default value is 1.</span></span>

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

### <span data-ttu-id="04ef1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ef1-116">-DefaultProfile</span></span>
<span data-ttu-id="04ef1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04ef1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04ef1-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="04ef1-118">-Location</span></span>
<span data-ttu-id="04ef1-119">Określa lokalizację nowego obszaru wdrożenia w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="04ef1-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="04ef1-120">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="04ef1-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="04ef1-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04ef1-121">-VirtualNetwork</span></span>
<span data-ttu-id="04ef1-122">Konfiguracja sieci wirtualnej w obszarze wdrażania zarządzania usługą Azure API.</span><span class="sxs-lookup"><span data-stu-id="04ef1-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="04ef1-123">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="04ef1-123">Default value is $null.</span></span>

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

### <span data-ttu-id="04ef1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ef1-124">CommonParameters</span></span>
<span data-ttu-id="04ef1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ef1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ef1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ef1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ef1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04ef1-127">INPUTS</span></span>

### <span data-ttu-id="04ef1-128">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04ef1-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="04ef1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04ef1-129">OUTPUTS</span></span>

### <span data-ttu-id="04ef1-130">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="04ef1-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="04ef1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04ef1-131">NOTES</span></span>

## <span data-ttu-id="04ef1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04ef1-132">RELATED LINKS</span></span>

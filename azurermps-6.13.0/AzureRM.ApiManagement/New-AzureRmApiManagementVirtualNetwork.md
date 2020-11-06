---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: abfcbec55ba3f53986a63a8c0964320c10fc91ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550400"
---
# <span data-ttu-id="633ad-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="633ad-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="633ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="633ad-102">SYNOPSIS</span></span>
<span data-ttu-id="633ad-103">Tworzy wystąpienie PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="633ad-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="633ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="633ad-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="633ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="633ad-105">DESCRIPTION</span></span>
<span data-ttu-id="633ad-106">Polecenie cmdlet **New-AzureRmApiManagementVirtualNetwork** jest poleceniem pomagającym w celu utworzenia wystąpienia **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="633ad-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="633ad-107">To polecenie jest używane w przypadku polecenia cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="633ad-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="633ad-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="633ad-108">EXAMPLES</span></span>

### <span data-ttu-id="633ad-109">Przykład 1. Tworzenie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="633ad-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="633ad-110">W tym przykładzie jest tworzona Sieć wirtualna, a następnie jest wywoływana funkcja cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="633ad-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="633ad-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="633ad-111">PARAMETERS</span></span>

### <span data-ttu-id="633ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633ad-112">-DefaultProfile</span></span>
<span data-ttu-id="633ad-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="633ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="633ad-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="633ad-114">-Location</span></span>
<span data-ttu-id="633ad-115">Określa lokalizację w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="633ad-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="633ad-116">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="633ad-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="633ad-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="633ad-117">-SubnetResourceId</span></span>
<span data-ttu-id="633ad-118">Określa identyfikator zasobu podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="633ad-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="633ad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633ad-119">CommonParameters</span></span>
<span data-ttu-id="633ad-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="633ad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633ad-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="633ad-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633ad-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="633ad-122">INPUTS</span></span>

### <span data-ttu-id="633ad-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="633ad-123">None</span></span>

## <span data-ttu-id="633ad-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="633ad-124">OUTPUTS</span></span>

### <span data-ttu-id="633ad-125">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="633ad-125">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="633ad-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="633ad-126">NOTES</span></span>

## <span data-ttu-id="633ad-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="633ad-127">RELATED LINKS</span></span>

[<span data-ttu-id="633ad-128">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="633ad-128">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


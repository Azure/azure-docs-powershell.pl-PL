---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554324"
---
# <span data-ttu-id="f300b-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f300b-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="f300b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f300b-102">SYNOPSIS</span></span>
<span data-ttu-id="f300b-103">Tworzy wystąpienie PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="f300b-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f300b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f300b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f300b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f300b-105">DESCRIPTION</span></span>
<span data-ttu-id="f300b-106">Polecenie cmdlet **New-AzureRmApiManagementVirtualNetwork** jest poleceniem pomagającym w celu utworzenia wystąpienia **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="f300b-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="f300b-107">To polecenie jest używane w przypadku polecenia cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="f300b-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="f300b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f300b-108">EXAMPLES</span></span>

### <span data-ttu-id="f300b-109">Przykład 1. Tworzenie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f300b-109">Example 1: Create a virtual network</span></span>
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

<span data-ttu-id="f300b-110">W tym przykładzie jest tworzona Sieć wirtualna, a następnie jest wywoływana funkcja cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="f300b-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="f300b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f300b-111">PARAMETERS</span></span>

### <span data-ttu-id="f300b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f300b-112">-DefaultProfile</span></span>
<span data-ttu-id="f300b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f300b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f300b-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f300b-114">-Location</span></span>
<span data-ttu-id="f300b-115">Określa lokalizację w obsługiwanym regionie usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f300b-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="f300b-116">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | gdzie {$ _. ResourceTypes [0]. ResourceTypeName-EQ "usługa"} | Lokalizacje Select-Object</span><span class="sxs-lookup"><span data-stu-id="f300b-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f300b-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="f300b-117">-SubnetResourceId</span></span>
<span data-ttu-id="f300b-118">Określa identyfikator zasobu podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f300b-118">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f300b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f300b-119">CommonParameters</span></span>
<span data-ttu-id="f300b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f300b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f300b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f300b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f300b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f300b-122">INPUTS</span></span>

### <span data-ttu-id="f300b-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f300b-123">None</span></span>
<span data-ttu-id="f300b-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f300b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f300b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f300b-125">OUTPUTS</span></span>

### <span data-ttu-id="f300b-126">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f300b-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="f300b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f300b-127">NOTES</span></span>

## <span data-ttu-id="f300b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f300b-128">RELATED LINKS</span></span>

[<span data-ttu-id="f300b-129">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f300b-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


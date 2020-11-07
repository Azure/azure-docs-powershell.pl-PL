---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869471"
---
# <span data-ttu-id="94c33-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94c33-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="94c33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94c33-102">SYNOPSIS</span></span>
<span data-ttu-id="94c33-103">Tworzy wystąpienie PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="94c33-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="94c33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94c33-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94c33-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94c33-105">DESCRIPTION</span></span>
<span data-ttu-id="94c33-106">Polecenie cmdlet **New-AzApiManagementVirtualNetwork** jest poleceniem pomagającym w celu utworzenia wystąpienia **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="94c33-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="94c33-107">To polecenie jest używane w przypadku polecenia cmdlet **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="94c33-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="94c33-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94c33-108">EXAMPLES</span></span>

### <span data-ttu-id="94c33-109">Przykład 1. Tworzenie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="94c33-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="94c33-110">W tym przykładzie jest tworzona Sieć wirtualna, a następnie jest wywoływana funkcja cmdlet **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="94c33-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="94c33-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94c33-111">PARAMETERS</span></span>

### <span data-ttu-id="94c33-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c33-112">-DefaultProfile</span></span>
<span data-ttu-id="94c33-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94c33-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94c33-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="94c33-114">-SubnetResourceId</span></span>
<span data-ttu-id="94c33-115">Określa identyfikator zasobu podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94c33-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="94c33-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c33-116">CommonParameters</span></span>
<span data-ttu-id="94c33-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c33-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c33-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c33-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c33-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94c33-119">INPUTS</span></span>

### <span data-ttu-id="94c33-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="94c33-120">None</span></span>

## <span data-ttu-id="94c33-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94c33-121">OUTPUTS</span></span>

### <span data-ttu-id="94c33-122">Microsoft. Azure. Commands. ApiManagement. models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="94c33-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="94c33-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94c33-123">NOTES</span></span>

## <span data-ttu-id="94c33-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94c33-124">RELATED LINKS</span></span>

[<span data-ttu-id="94c33-125">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="94c33-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)


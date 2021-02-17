---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 496e65438a2c0ef5f09bbf961535eaa842062f25
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400896"
---
# <span data-ttu-id="03445-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03445-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="03445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03445-102">SYNOPSIS</span></span>
<span data-ttu-id="03445-103">Tworzy wystąpienie obiektu PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="03445-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="03445-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03445-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03445-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="03445-105">DESCRIPTION</span></span>
<span data-ttu-id="03445-106">Polecenie cmdlet **New-AzApiManagementVirtualNetwork** to polecenie pomocne podczas tworzenia wystąpienia polecenia **PsApiManagementVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="03445-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="03445-107">To polecenie jest używane z poleceniem cmdlet **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="03445-107">This command is used with **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="03445-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03445-108">EXAMPLES</span></span>

### <span data-ttu-id="03445-109">Przykład 1. Tworzenie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="03445-109">Example 1: Create a virtual network</span></span>
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
PS C:\>Set-AzApiManagement -ApiManagement $service
```

<span data-ttu-id="03445-110">W tym przykładzie jest owana sieć wirtualna, a następnie jest zwracane polecenie cmdlet **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="03445-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="03445-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03445-111">PARAMETERS</span></span>

### <span data-ttu-id="03445-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03445-112">-DefaultProfile</span></span>
<span data-ttu-id="03445-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03445-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03445-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="03445-114">-SubnetResourceId</span></span>
<span data-ttu-id="03445-115">Określa identyfikator zasobu podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="03445-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="03445-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03445-116">CommonParameters</span></span>
<span data-ttu-id="03445-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03445-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03445-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03445-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03445-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03445-119">INPUTS</span></span>

### <span data-ttu-id="03445-120">Brak</span><span class="sxs-lookup"><span data-stu-id="03445-120">None</span></span>

## <span data-ttu-id="03445-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03445-121">OUTPUTS</span></span>

### <span data-ttu-id="03445-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03445-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="03445-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03445-123">NOTES</span></span>

## <span data-ttu-id="03445-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03445-124">RELATED LINKS</span></span>

[<span data-ttu-id="03445-125">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="03445-125">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


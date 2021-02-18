---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239691"
---
# <span data-ttu-id="bfb6e-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bfb6e-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="bfb6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb6e-103">Tworzy wystąpienie obiektu PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="bfb6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bfb6e-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfb6e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bfb6e-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb6e-106">Polecenie cmdlet **New-AzApiManagementVirtualNetwork** to polecenie pomocne podczas tworzenia wystąpienia polecenia **PsApiManagementVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="bfb6e-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="bfb6e-107">To polecenie jest używane z **poleceniami cmdlet Set-AzApiManagement** i **New-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="bfb6e-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="bfb6e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bfb6e-108">EXAMPLES</span></span>

### <span data-ttu-id="bfb6e-109">Przykład 1. Tworzenie sieci wirtualnej i aktualizowanie istniejącej usługi APIM do sieci VNET</span><span class="sxs-lookup"><span data-stu-id="bfb6e-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="bfb6e-110">W tym przykładzie jest owana sieć wirtualna, a następnie jest zwracane polecenie cmdlet **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="bfb6e-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="bfb6e-111">Przykład 2. Tworzenie usługi zarządzania interfejsem API dla zewnętrznej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bfb6e-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="bfb6e-112">W tym przykładzie w trybie tworzenia nowej usługi APIM w sieci `External` wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bfb6e-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="bfb6e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfb6e-113">PARAMETERS</span></span>

### <span data-ttu-id="bfb6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb6e-114">-DefaultProfile</span></span>
<span data-ttu-id="bfb6e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb6e-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="bfb6e-116">-SubnetResourceId</span></span>
<span data-ttu-id="bfb6e-117">Określa identyfikator zasobu podsieci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="bfb6e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb6e-118">CommonParameters</span></span>
<span data-ttu-id="bfb6e-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb6e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb6e-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfb6e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb6e-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfb6e-121">INPUTS</span></span>

### <span data-ttu-id="bfb6e-122">Brak</span><span class="sxs-lookup"><span data-stu-id="bfb6e-122">None</span></span>

## <span data-ttu-id="bfb6e-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bfb6e-123">OUTPUTS</span></span>

### <span data-ttu-id="bfb6e-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bfb6e-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="bfb6e-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bfb6e-125">NOTES</span></span>

## <span data-ttu-id="bfb6e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfb6e-126">RELATED LINKS</span></span>

<span data-ttu-id="bfb6e-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="bfb6e-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>


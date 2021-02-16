---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179858"
---
# <span data-ttu-id="33ad4-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="33ad4-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="33ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="33ad4-103">Lista dostępnych usług punktu końcowego dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="33ad4-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="33ad4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33ad4-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33ad4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="33ad4-105">DESCRIPTION</span></span>
<span data-ttu-id="33ad4-106">Get-AzVirtualNetworkAvailableEndpointService listę usług punktu końcowego dostępnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="33ad4-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="33ad4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33ad4-107">EXAMPLES</span></span>

### <span data-ttu-id="33ad4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33ad4-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="33ad4-109">Pobiera dostępne usługi punktu końcowego w regionie Zachód.</span><span class="sxs-lookup"><span data-stu-id="33ad4-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="33ad4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33ad4-110">PARAMETERS</span></span>

### <span data-ttu-id="33ad4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ad4-111">-DefaultProfile</span></span>
<span data-ttu-id="33ad4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33ad4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33ad4-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="33ad4-113">-Location</span></span>
<span data-ttu-id="33ad4-114">Lokalizacja, z których mają być pobierane usługi punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="33ad4-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ad4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ad4-115">CommonParameters</span></span>
<span data-ttu-id="33ad4-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ad4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ad4-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33ad4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ad4-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33ad4-118">INPUTS</span></span>

### <span data-ttu-id="33ad4-119">System.String</span><span class="sxs-lookup"><span data-stu-id="33ad4-119">System.String</span></span>

## <span data-ttu-id="33ad4-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33ad4-120">OUTPUTS</span></span>

### <span data-ttu-id="33ad4-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="33ad4-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="33ad4-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33ad4-122">NOTES</span></span>

## <span data-ttu-id="33ad4-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33ad4-123">RELATED LINKS</span></span>

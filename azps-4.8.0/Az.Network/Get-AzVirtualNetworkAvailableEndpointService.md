---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220005"
---
# <span data-ttu-id="34bb5-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="34bb5-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="34bb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="34bb5-103">Wyświetla listę dostępnych usług punktu końcowego dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="34bb5-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="34bb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34bb5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34bb5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34bb5-105">DESCRIPTION</span></span>
<span data-ttu-id="34bb5-106">Get-AzVirtualNetworkAvailableEndpointService wyświetla listę usług punktu końcowego dostępnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="34bb5-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="34bb5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34bb5-107">EXAMPLES</span></span>

### <span data-ttu-id="34bb5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34bb5-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="34bb5-109">Pobiera dostępne usługi punktu końcowego w regionie zachód.</span><span class="sxs-lookup"><span data-stu-id="34bb5-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="34bb5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34bb5-110">PARAMETERS</span></span>

### <span data-ttu-id="34bb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34bb5-111">-DefaultProfile</span></span>
<span data-ttu-id="34bb5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34bb5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34bb5-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="34bb5-113">-Location</span></span>
<span data-ttu-id="34bb5-114">Lokalizacja, z której mają zostać pobrane usługi punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="34bb5-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="34bb5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bb5-115">CommonParameters</span></span>
<span data-ttu-id="34bb5-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bb5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bb5-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34bb5-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bb5-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34bb5-118">INPUTS</span></span>

### <span data-ttu-id="34bb5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="34bb5-119">System.String</span></span>

## <span data-ttu-id="34bb5-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34bb5-120">OUTPUTS</span></span>

### <span data-ttu-id="34bb5-121">Microsoft. Azure. Commands. Network. models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="34bb5-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="34bb5-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34bb5-122">NOTES</span></span>

## <span data-ttu-id="34bb5-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34bb5-123">RELATED LINKS</span></span>

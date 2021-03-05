---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: ae7c7bdd41f21c3f9263a8ea65aab722512543f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993903"
---
# <span data-ttu-id="14bf4-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="14bf4-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="14bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="14bf4-103">Zwracanie dostępnych typów prywatnych punktów końcowych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="14bf4-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="14bf4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14bf4-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14bf4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="14bf4-106">Polecenie **cmdlet Get-AzAvailablePrivateEndpointType** zwraca wszystkie dostępne typy prywatnych punktów końcowych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="14bf4-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="14bf4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="14bf4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14bf4-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="14bf4-109">W tym przykładzie są zwracane wszystkie dostępne prywatne typy punktów końcowych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="14bf4-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="14bf4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="14bf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14bf4-111">-DefaultProfile</span></span>
<span data-ttu-id="14bf4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14bf4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14bf4-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="14bf4-113">-Location</span></span>
<span data-ttu-id="14bf4-114">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="14bf4-114">The location.</span></span>

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

### <span data-ttu-id="14bf4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14bf4-115">-ResourceGroupName</span></span>
<span data-ttu-id="14bf4-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14bf4-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14bf4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14bf4-117">CommonParameters</span></span>
<span data-ttu-id="14bf4-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14bf4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14bf4-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14bf4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14bf4-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14bf4-120">INPUTS</span></span>

### <span data-ttu-id="14bf4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="14bf4-121">System.String</span></span>

## <span data-ttu-id="14bf4-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14bf4-122">OUTPUTS</span></span>

### <span data-ttu-id="14bf4-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="14bf4-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="14bf4-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14bf4-124">NOTES</span></span>

## <span data-ttu-id="14bf4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14bf4-125">RELATED LINKS</span></span>

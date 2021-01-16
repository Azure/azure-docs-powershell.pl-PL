---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338077"
---
# <span data-ttu-id="755b1-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="755b1-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="755b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="755b1-102">SYNOPSIS</span></span>
<span data-ttu-id="755b1-103">Zwracają dostępne typy prywatnego punktu końcowego w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="755b1-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="755b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="755b1-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="755b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="755b1-105">DESCRIPTION</span></span>
<span data-ttu-id="755b1-106">Polecenie cmdlet **Get-AzAvailablePrivateEndpointType** zwraca wszystkie dostępne typy prywatnych punktów końcowych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="755b1-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="755b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="755b1-107">EXAMPLES</span></span>

### <span data-ttu-id="755b1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="755b1-108">Example 1</span></span>
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

<span data-ttu-id="755b1-109">W tym przykładzie są zwracane wszystkie dostępne typy prywatnych punktów końcowych w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="755b1-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="755b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="755b1-110">PARAMETERS</span></span>

### <span data-ttu-id="755b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755b1-111">-DefaultProfile</span></span>
<span data-ttu-id="755b1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="755b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="755b1-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="755b1-113">-Location</span></span>
<span data-ttu-id="755b1-114">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="755b1-114">The location.</span></span>

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

### <span data-ttu-id="755b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="755b1-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="755b1-116">The resource group name.</span></span>

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

### <span data-ttu-id="755b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755b1-117">CommonParameters</span></span>
<span data-ttu-id="755b1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755b1-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="755b1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755b1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="755b1-120">INPUTS</span></span>

### <span data-ttu-id="755b1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="755b1-121">System.String</span></span>

## <span data-ttu-id="755b1-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="755b1-122">OUTPUTS</span></span>

### <span data-ttu-id="755b1-123">Microsoft. Azure. Commands. Network. models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="755b1-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="755b1-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="755b1-124">NOTES</span></span>

## <span data-ttu-id="755b1-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="755b1-125">RELATED LINKS</span></span>

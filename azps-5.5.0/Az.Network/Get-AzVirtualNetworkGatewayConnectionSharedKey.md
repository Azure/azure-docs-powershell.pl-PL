---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189714"
---
# <span data-ttu-id="b41ef-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b41ef-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b41ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b41ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b41ef-103">Wyświetla klucz udostępniony używany dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="b41ef-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="b41ef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b41ef-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b41ef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b41ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b41ef-106">Wyświetla klucz udostępniony używany dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="b41ef-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="b41ef-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b41ef-107">EXAMPLES</span></span>

### <span data-ttu-id="b41ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b41ef-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="b41ef-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b41ef-109">PARAMETERS</span></span>

### <span data-ttu-id="b41ef-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41ef-110">-DefaultProfile</span></span>
<span data-ttu-id="b41ef-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b41ef-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b41ef-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b41ef-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b41ef-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b41ef-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b41ef-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41ef-114">CommonParameters</span></span>
<span data-ttu-id="b41ef-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b41ef-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41ef-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b41ef-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41ef-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b41ef-117">INPUTS</span></span>

### <span data-ttu-id="b41ef-118">System.String</span><span class="sxs-lookup"><span data-stu-id="b41ef-118">System.String</span></span>

## <span data-ttu-id="b41ef-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b41ef-119">OUTPUTS</span></span>

### <span data-ttu-id="b41ef-120">System.String</span><span class="sxs-lookup"><span data-stu-id="b41ef-120">System.String</span></span>

## <span data-ttu-id="b41ef-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b41ef-121">NOTES</span></span>

## <span data-ttu-id="b41ef-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b41ef-122">RELATED LINKS</span></span>

[<span data-ttu-id="b41ef-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b41ef-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b41ef-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b41ef-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)

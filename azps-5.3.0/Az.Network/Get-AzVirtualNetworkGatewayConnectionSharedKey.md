---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381017"
---
# <span data-ttu-id="7e3b7-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7e3b7-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="7e3b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3b7-103">Umożliwia wyświetlenie klucza współużytkowanego dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="7e3b7-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="7e3b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e3b7-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e3b7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e3b7-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3b7-106">Umożliwia wyświetlenie klucza współużytkowanego dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="7e3b7-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="7e3b7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e3b7-107">EXAMPLES</span></span>

### <span data-ttu-id="7e3b7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e3b7-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="7e3b7-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e3b7-109">PARAMETERS</span></span>

### <span data-ttu-id="7e3b7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3b7-110">-DefaultProfile</span></span>
<span data-ttu-id="7e3b7-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3b7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e3b7-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e3b7-112">-Name</span></span>
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

### <span data-ttu-id="7e3b7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3b7-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7e3b7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3b7-114">CommonParameters</span></span>
<span data-ttu-id="7e3b7-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3b7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3b7-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e3b7-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3b7-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e3b7-117">INPUTS</span></span>

### <span data-ttu-id="7e3b7-118">System. String</span><span class="sxs-lookup"><span data-stu-id="7e3b7-118">System.String</span></span>

## <span data-ttu-id="7e3b7-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e3b7-119">OUTPUTS</span></span>

### <span data-ttu-id="7e3b7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7e3b7-120">System.String</span></span>

## <span data-ttu-id="7e3b7-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e3b7-121">NOTES</span></span>

## <span data-ttu-id="7e3b7-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e3b7-122">RELATED LINKS</span></span>

[<span data-ttu-id="7e3b7-123">Resetowanie — AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7e3b7-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="7e3b7-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7e3b7-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)

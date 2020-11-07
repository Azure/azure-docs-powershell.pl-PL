---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: f8b41145c29d0eb3b2485fb1eb6b969574686b08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870184"
---
# <span data-ttu-id="adf05-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="adf05-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="adf05-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="adf05-102">SYNOPSIS</span></span>
<span data-ttu-id="adf05-103">Uzyskaj tożsamość przypisaną do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="adf05-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="adf05-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="adf05-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adf05-105">Opis</span><span class="sxs-lookup"><span data-stu-id="adf05-105">DESCRIPTION</span></span>
<span data-ttu-id="adf05-106">Polecenie cmdlet **Get-AzExpressRoutePortIdentity** pobiera tożsamość przypisaną do lokalnego obiektu usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="adf05-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="adf05-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="adf05-107">EXAMPLES</span></span>

### <span data-ttu-id="adf05-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="adf05-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="adf05-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="adf05-109">PARAMETERS</span></span>

### <span data-ttu-id="adf05-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf05-110">-DefaultProfile</span></span>
<span data-ttu-id="adf05-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="adf05-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adf05-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="adf05-112">-ExpressRoutePort</span></span>
<span data-ttu-id="adf05-113">Port ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="adf05-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adf05-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf05-114">CommonParameters</span></span>
<span data-ttu-id="adf05-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf05-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf05-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adf05-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf05-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adf05-117">INPUTS</span></span>

### <span data-ttu-id="adf05-118">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="adf05-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="adf05-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="adf05-119">OUTPUTS</span></span>

### <span data-ttu-id="adf05-120">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="adf05-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="adf05-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="adf05-121">NOTES</span></span>

## <span data-ttu-id="adf05-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adf05-122">RELATED LINKS</span></span>
[<span data-ttu-id="adf05-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="adf05-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="adf05-124">Nowe — AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="adf05-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="adf05-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="adf05-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709551"
---
# <span data-ttu-id="623cd-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="623cd-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="623cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="623cd-102">SYNOPSIS</span></span>
<span data-ttu-id="623cd-103">Pobiera połączenie z usługą Azure ExpressRoute krzyżowe z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="623cd-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="623cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="623cd-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="623cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="623cd-105">DESCRIPTION</span></span>
<span data-ttu-id="623cd-106">Polecenie cmdlet **Get-AzExpressRouteCrossConnection** służy do pobierania ExpressRoute obiektu połączenia krzyżowego z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="623cd-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="623cd-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="623cd-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="623cd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="623cd-108">EXAMPLES</span></span>

### <span data-ttu-id="623cd-109">Przykład 1. Uzyskaj połączenie krzyżowe ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="623cd-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="623cd-110">Przykład 2: wyświetlanie połączeń krzyżowych z ExpressRoute przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="623cd-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="623cd-111">To polecenie cmdlet spowoduje wyświetlenie wszystkich połączeń krzyżowych ExpressRoute, które zaczynają się od ciągu "test".</span><span class="sxs-lookup"><span data-stu-id="623cd-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="623cd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="623cd-112">PARAMETERS</span></span>

### <span data-ttu-id="623cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623cd-113">-DefaultProfile</span></span>
<span data-ttu-id="623cd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="623cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="623cd-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="623cd-115">-Name</span></span>
<span data-ttu-id="623cd-116">Nazwa połączenia krzyżowego ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="623cd-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="623cd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623cd-117">-ResourceGroupName</span></span>
<span data-ttu-id="623cd-118">Nazwa grupy zasobów zawierającej połączenie krzyżowe ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="623cd-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="623cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623cd-119">CommonParameters</span></span>
<span data-ttu-id="623cd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623cd-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="623cd-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623cd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="623cd-122">INPUTS</span></span>

### <span data-ttu-id="623cd-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="623cd-123">None</span></span>
<span data-ttu-id="623cd-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="623cd-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="623cd-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="623cd-125">OUTPUTS</span></span>

### <span data-ttu-id="623cd-126">Microsoft. Azure. Commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="623cd-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="623cd-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="623cd-127">NOTES</span></span>

## <span data-ttu-id="623cd-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="623cd-128">RELATED LINKS</span></span>

[<span data-ttu-id="623cd-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="623cd-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
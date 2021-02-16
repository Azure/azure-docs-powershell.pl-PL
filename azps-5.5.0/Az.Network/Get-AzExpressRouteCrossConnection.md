---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187210"
---
# <span data-ttu-id="2e2a9-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2e2a9-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="2e2a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2a9-103">Pobiera połączenie krzyżowe usługi Azure ExpressRoute z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="2e2a9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2e2a9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e2a9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2e2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="2e2a9-106">Polecenie **cmdlet Get-AzExpressRouteCrossConnection** służy do pobierania obiektu połączenia krzyżowego usługi ExpressRoute z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="2e2a9-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2e2a9-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="2e2a9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2e2a9-108">EXAMPLES</span></span>

### <span data-ttu-id="2e2a9-109">Przykład 1. Uzyskiwanie połączenia krzyżowego expressRoute</span><span class="sxs-lookup"><span data-stu-id="2e2a9-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="2e2a9-110">Przykład 2. Lista połączeń krzyżowych usługi ExpressRoute przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="2e2a9-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="2e2a9-111">To polecenie cmdlet spowoduje listę wszystkich połączeń krzyżowych expressRoute, które zaczynają się od "testu".</span><span class="sxs-lookup"><span data-stu-id="2e2a9-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="2e2a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e2a9-112">PARAMETERS</span></span>

### <span data-ttu-id="2e2a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2a9-113">-DefaultProfile</span></span>
<span data-ttu-id="2e2a9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e2a9-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2e2a9-115">-Name</span></span>
<span data-ttu-id="2e2a9-116">Nazwa połączenia krzyżowego expressRoute.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="2e2a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e2a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e2a9-118">Nazwa grupy zasobów zawierającej połączenie krzyżowe expressRoute.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="2e2a9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2a9-119">CommonParameters</span></span>
<span data-ttu-id="2e2a9-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2a9-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e2a9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2a9-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e2a9-122">INPUTS</span></span>

### <span data-ttu-id="2e2a9-123">Brak</span><span class="sxs-lookup"><span data-stu-id="2e2a9-123">None</span></span>
<span data-ttu-id="2e2a9-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e2a9-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e2a9-125">OUTPUTS</span></span>

### <span data-ttu-id="2e2a9-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2e2a9-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="2e2a9-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2e2a9-127">NOTES</span></span>

## <span data-ttu-id="2e2a9-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e2a9-128">RELATED LINKS</span></span>

[<span data-ttu-id="2e2a9-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2e2a9-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
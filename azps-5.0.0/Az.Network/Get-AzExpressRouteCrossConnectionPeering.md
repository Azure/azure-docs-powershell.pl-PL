---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232601"
---
# <span data-ttu-id="c551f-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c551f-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="c551f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c551f-102">SYNOPSIS</span></span>
<span data-ttu-id="c551f-103">Pobiera konfigurację komunikacji równorzędnej z ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c551f-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="c551f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c551f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c551f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c551f-105">DESCRIPTION</span></span>
<span data-ttu-id="c551f-106">Polecenie cmdlet **Get-AzExpressRouteCrossConnectionPeering** Pobiera konfigurację relacji komunikacji równorzędnej dla połączenia krzyżowego ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c551f-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="c551f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c551f-107">EXAMPLES</span></span>

### <span data-ttu-id="c551f-108">Przykład 1: Wyświetlanie konfiguracji komunikacji równorzędnej dla połączenia z ExpressRoute krzyżowej</span><span class="sxs-lookup"><span data-stu-id="c551f-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="c551f-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c551f-109">PARAMETERS</span></span>

### <span data-ttu-id="c551f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c551f-110">-DefaultProfile</span></span>
<span data-ttu-id="c551f-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c551f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c551f-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c551f-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="c551f-113">Obiekt ExpressRoute Cross (połączenie krzyżowe) zawierający konfigurację komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="c551f-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c551f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c551f-114">-Name</span></span>
<span data-ttu-id="c551f-115">Nazwa konfiguracji elementu równorzędnego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c551f-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="c551f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c551f-116">CommonParameters</span></span>
<span data-ttu-id="c551f-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c551f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c551f-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c551f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c551f-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c551f-119">INPUTS</span></span>

### <span data-ttu-id="c551f-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c551f-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="c551f-121">Parametr "ExpressRouteCrossConnection" akceptuje wartość typu "PSExpressRouteCrossConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c551f-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="c551f-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c551f-122">OUTPUTS</span></span>

### <span data-ttu-id="c551f-123">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="c551f-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="c551f-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c551f-124">NOTES</span></span>

## <span data-ttu-id="c551f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c551f-125">RELATED LINKS</span></span>

[<span data-ttu-id="c551f-126">Dodaj-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c551f-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="c551f-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c551f-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="c551f-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c551f-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="c551f-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c551f-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 99142e3dd33d84e11f326258450d92a58fe70e20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709548"
---
# <span data-ttu-id="a779e-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a779e-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="a779e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a779e-102">SYNOPSIS</span></span>
<span data-ttu-id="a779e-103">Pobiera konfigurację komunikacji równorzędnej z ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a779e-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="a779e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a779e-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a779e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a779e-105">DESCRIPTION</span></span>
<span data-ttu-id="a779e-106">Polecenie cmdlet **Get-AzExpressRouteCrossConnectionPeering** Pobiera konfigurację relacji komunikacji równorzędnej dla połączenia krzyżowego ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a779e-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="a779e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a779e-107">EXAMPLES</span></span>

### <span data-ttu-id="a779e-108">Przykład 1: Wyświetlanie konfiguracji komunikacji równorzędnej dla połączenia z ExpressRoute krzyżowej</span><span class="sxs-lookup"><span data-stu-id="a779e-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="a779e-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a779e-109">PARAMETERS</span></span>

### <span data-ttu-id="a779e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a779e-110">-DefaultProfile</span></span>
<span data-ttu-id="a779e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a779e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a779e-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a779e-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="a779e-113">Obiekt ExpressRoute Cross (połączenie krzyżowe) zawierający konfigurację komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="a779e-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="a779e-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a779e-114">-Name</span></span>
<span data-ttu-id="a779e-115">Nazwa konfiguracji elementu równorzędnego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a779e-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="a779e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a779e-116">CommonParameters</span></span>
<span data-ttu-id="a779e-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a779e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a779e-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a779e-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a779e-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a779e-119">INPUTS</span></span>

### <span data-ttu-id="a779e-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a779e-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="a779e-121">Parametr "ExpressRouteCrossConnection" akceptuje wartość typu "PSExpressRouteCrossConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a779e-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="a779e-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a779e-122">OUTPUTS</span></span>

### <span data-ttu-id="a779e-123">Microsoft. Azure. Commands. Network. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a779e-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="a779e-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a779e-124">NOTES</span></span>

## <span data-ttu-id="a779e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a779e-125">RELATED LINKS</span></span>

[<span data-ttu-id="a779e-126">Dodaj-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a779e-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a779e-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a779e-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a779e-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a779e-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="a779e-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a779e-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 44a7dd8c0fbb3193ac514f9c1b447394b29574f3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400063"
---
# <span data-ttu-id="b2fbb-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b2fbb-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="b2fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="b2fbb-103">Usuwa konfigurację komunikacji równorzędnej połączenia krzyżowego usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="b2fbb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2fbb-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2fbb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="b2fbb-106">Polecenie **cmdlet Remove-AzExpressRouteCrossConnectionPeering** usuwa konfigurację komunikacji równorzędnej połączenia krzyżowego usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="b2fbb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="b2fbb-108">Przykład 1. Usuwanie konfiguracji komunikacji równorzędnej z połączenia krzyżowego usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b2fbb-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="b2fbb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2fbb-109">PARAMETERS</span></span>

### <span data-ttu-id="b2fbb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2fbb-110">-DefaultProfile</span></span>
<span data-ttu-id="b2fbb-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2fbb-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b2fbb-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="b2fbb-113">Połączenie krzyżowe usługi ExpressRoute zawierające konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="b2fbb-114">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b2fbb-114">-Force</span></span>
<span data-ttu-id="b2fbb-115">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="b2fbb-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2fbb-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b2fbb-116">-Name</span></span>
<span data-ttu-id="b2fbb-117">Nazwa konfiguracji komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2fbb-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b2fbb-118">-PeerAddressType</span></span>
<span data-ttu-id="b2fbb-119">Rodzina adresów komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="b2fbb-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2fbb-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2fbb-120">-Confirm</span></span>
<span data-ttu-id="b2fbb-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2fbb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2fbb-122">-WhatIf</span></span>
<span data-ttu-id="b2fbb-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2fbb-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2fbb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2fbb-125">CommonParameters</span></span>
<span data-ttu-id="b2fbb-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2fbb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2fbb-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2fbb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2fbb-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2fbb-128">INPUTS</span></span>

### <span data-ttu-id="b2fbb-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b2fbb-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="b2fbb-130">Parametr "ExpressRouteCrossConnection" przyjmuje wartość typu "PSExpressRouteCrossConnection" z potoku</span><span class="sxs-lookup"><span data-stu-id="b2fbb-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="b2fbb-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2fbb-131">OUTPUTS</span></span>

### <span data-ttu-id="b2fbb-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b2fbb-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="b2fbb-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2fbb-133">NOTES</span></span>

## <span data-ttu-id="b2fbb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2fbb-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2fbb-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b2fbb-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)



[<span data-ttu-id="b2fbb-136">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b2fbb-136">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="b2fbb-137">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b2fbb-137">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)

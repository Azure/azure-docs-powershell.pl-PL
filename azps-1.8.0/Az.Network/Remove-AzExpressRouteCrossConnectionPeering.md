---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b991b26d8d6fc7a7cfd33ab051619b7192ae0aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709141"
---
# <span data-ttu-id="2eac9-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2eac9-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="2eac9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eac9-102">SYNOPSIS</span></span>
<span data-ttu-id="2eac9-103">Usuwa konfigurację komunikacji równorzędnej ExpressRoute krzyż.</span><span class="sxs-lookup"><span data-stu-id="2eac9-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="2eac9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eac9-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eac9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2eac9-105">DESCRIPTION</span></span>
<span data-ttu-id="2eac9-106">Polecenie cmdlet **Remove-AzExpressRouteCrossConnectionPeering** usuwa konfigurację komunikacji równorzędnej z ExpressRoute połączenia krzyżowego.</span><span class="sxs-lookup"><span data-stu-id="2eac9-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="2eac9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eac9-107">EXAMPLES</span></span>

### <span data-ttu-id="2eac9-108">Przykład 1: Usuwanie konfiguracji równorzędnej z połączenia z ExpressRoute krzyżowej</span><span class="sxs-lookup"><span data-stu-id="2eac9-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="2eac9-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eac9-109">PARAMETERS</span></span>

### <span data-ttu-id="2eac9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eac9-110">-DefaultProfile</span></span>
<span data-ttu-id="2eac9-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2eac9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eac9-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2eac9-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="2eac9-113">Połączenie krzyżowe z ExpressRoute, zawierające konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2eac9-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="2eac9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2eac9-114">-Force</span></span>
<span data-ttu-id="2eac9-115">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="2eac9-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="2eac9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2eac9-116">-Name</span></span>
<span data-ttu-id="2eac9-117">Nazwa konfiguracji elementu równorzędnego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2eac9-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="2eac9-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="2eac9-118">-PeerAddressType</span></span>
<span data-ttu-id="2eac9-119">Rodzina adresów komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="2eac9-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="2eac9-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2eac9-120">-Confirm</span></span>
<span data-ttu-id="2eac9-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eac9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eac9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eac9-122">-WhatIf</span></span>
<span data-ttu-id="2eac9-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eac9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2eac9-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2eac9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eac9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eac9-125">CommonParameters</span></span>
<span data-ttu-id="2eac9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eac9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eac9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eac9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eac9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eac9-128">INPUTS</span></span>

### <span data-ttu-id="2eac9-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2eac9-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="2eac9-130">Parametr "ExpressRouteCrossConnection" akceptuje wartość typu "PSExpressRouteCrossConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2eac9-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="2eac9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eac9-131">OUTPUTS</span></span>

### <span data-ttu-id="2eac9-132">Microsoft. Azure. Commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2eac9-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="2eac9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eac9-133">NOTES</span></span>

## <span data-ttu-id="2eac9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eac9-134">RELATED LINKS</span></span>

[<span data-ttu-id="2eac9-135">Dodaj-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2eac9-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="2eac9-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2eac9-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="2eac9-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2eac9-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="2eac9-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2eac9-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)

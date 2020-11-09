---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309175"
---
# <span data-ttu-id="020ce-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="020ce-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="020ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="020ce-102">SYNOPSIS</span></span>
<span data-ttu-id="020ce-103">Usuwa konfigurację komunikacji równorzędnej ExpressRoute krzyż.</span><span class="sxs-lookup"><span data-stu-id="020ce-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="020ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="020ce-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="020ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="020ce-105">DESCRIPTION</span></span>
<span data-ttu-id="020ce-106">Polecenie cmdlet **Remove-AzExpressRouteCrossConnectionPeering** usuwa konfigurację komunikacji równorzędnej z ExpressRoute połączenia krzyżowego.</span><span class="sxs-lookup"><span data-stu-id="020ce-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="020ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="020ce-107">EXAMPLES</span></span>

### <span data-ttu-id="020ce-108">Przykład 1: Usuwanie konfiguracji równorzędnej z połączenia z ExpressRoute krzyżowej</span><span class="sxs-lookup"><span data-stu-id="020ce-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="020ce-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="020ce-109">PARAMETERS</span></span>

### <span data-ttu-id="020ce-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020ce-110">-DefaultProfile</span></span>
<span data-ttu-id="020ce-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="020ce-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="020ce-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="020ce-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="020ce-113">Połączenie krzyżowe z ExpressRoute, zawierające konfigurację komunikacji równorzędnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="020ce-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="020ce-114">-Force</span><span class="sxs-lookup"><span data-stu-id="020ce-114">-Force</span></span>
<span data-ttu-id="020ce-115">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="020ce-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="020ce-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="020ce-116">-Name</span></span>
<span data-ttu-id="020ce-117">Nazwa konfiguracji elementu równorzędnego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="020ce-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="020ce-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="020ce-118">-PeerAddressType</span></span>
<span data-ttu-id="020ce-119">Rodzina adresów komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="020ce-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="020ce-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="020ce-120">-Confirm</span></span>
<span data-ttu-id="020ce-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="020ce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020ce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020ce-122">-WhatIf</span></span>
<span data-ttu-id="020ce-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="020ce-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="020ce-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="020ce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020ce-125">CommonParameters</span></span>
<span data-ttu-id="020ce-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020ce-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="020ce-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020ce-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="020ce-128">INPUTS</span></span>

### <span data-ttu-id="020ce-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="020ce-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="020ce-130">Parametr "ExpressRouteCrossConnection" akceptuje wartość typu "PSExpressRouteCrossConnection" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="020ce-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="020ce-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="020ce-131">OUTPUTS</span></span>

### <span data-ttu-id="020ce-132">Microsoft. Azure. Commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="020ce-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="020ce-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="020ce-133">NOTES</span></span>

## <span data-ttu-id="020ce-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="020ce-134">RELATED LINKS</span></span>

[<span data-ttu-id="020ce-135">Dodaj-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="020ce-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="020ce-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="020ce-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="020ce-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="020ce-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="020ce-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="020ce-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)

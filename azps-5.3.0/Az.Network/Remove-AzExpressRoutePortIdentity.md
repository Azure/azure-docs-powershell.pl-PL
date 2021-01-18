---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500310"
---
# <span data-ttu-id="0033f-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0033f-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="0033f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0033f-102">SYNOPSIS</span></span>
<span data-ttu-id="0033f-103">Usuwa tożsamość z ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0033f-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="0033f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0033f-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0033f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0033f-105">DESCRIPTION</span></span>
<span data-ttu-id="0033f-106">Polecenie cmdlet **Remove-AzExpressRoutePortIdentity** usuwa tożsamość z lokalnego obiektu usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0033f-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="0033f-107">Użyj narzędzia **Remove-AzExpressRoutePort** , aby usunąć go z usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0033f-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="0033f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0033f-108">EXAMPLES</span></span>

### <span data-ttu-id="0033f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0033f-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="0033f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0033f-110">PARAMETERS</span></span>

### <span data-ttu-id="0033f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0033f-111">-DefaultProfile</span></span>
<span data-ttu-id="0033f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0033f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0033f-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0033f-113">-ExpressRoutePort</span></span>
<span data-ttu-id="0033f-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0033f-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="0033f-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0033f-115">-Confirm</span></span>
<span data-ttu-id="0033f-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0033f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0033f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0033f-117">-WhatIf</span></span>
<span data-ttu-id="0033f-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0033f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0033f-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0033f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0033f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0033f-120">CommonParameters</span></span>
<span data-ttu-id="0033f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0033f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0033f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0033f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="0033f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0033f-123">INPUTS</span></span>

### <span data-ttu-id="0033f-124">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0033f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="0033f-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0033f-125">OUTPUTS</span></span>

### <span data-ttu-id="0033f-126">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0033f-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="0033f-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0033f-127">NOTES</span></span>

## <span data-ttu-id="0033f-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0033f-128">RELATED LINKS</span></span>
[<span data-ttu-id="0033f-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0033f-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="0033f-130">Nowe — AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0033f-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="0033f-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="0033f-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

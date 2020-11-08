---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053016"
---
# <span data-ttu-id="b9fd5-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b9fd5-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="b9fd5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fd5-103">Usuwa tożsamość z ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="b9fd5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9fd5-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fd5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fd5-106">Polecenie cmdlet **Remove-AzExpressRoutePortIdentity** usuwa tożsamość z lokalnego obiektu usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="b9fd5-107">Użyj narzędzia **Remove-AzExpressRoutePort** , aby usunąć go z usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="b9fd5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9fd5-108">EXAMPLES</span></span>

### <span data-ttu-id="b9fd5-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9fd5-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="b9fd5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9fd5-110">PARAMETERS</span></span>

### <span data-ttu-id="b9fd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fd5-111">-DefaultProfile</span></span>
<span data-ttu-id="b9fd5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9fd5-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b9fd5-113">-ExpressRoutePort</span></span>
<span data-ttu-id="b9fd5-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b9fd5-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="b9fd5-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9fd5-115">-Confirm</span></span>
<span data-ttu-id="b9fd5-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9fd5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9fd5-117">-WhatIf</span></span>
<span data-ttu-id="b9fd5-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9fd5-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9fd5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fd5-120">CommonParameters</span></span>
<span data-ttu-id="b9fd5-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fd5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fd5-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9fd5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="b9fd5-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9fd5-123">INPUTS</span></span>

### <span data-ttu-id="b9fd5-124">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b9fd5-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b9fd5-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9fd5-125">OUTPUTS</span></span>

### <span data-ttu-id="b9fd5-126">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b9fd5-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b9fd5-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9fd5-127">NOTES</span></span>

## <span data-ttu-id="b9fd5-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9fd5-128">RELATED LINKS</span></span>
[<span data-ttu-id="b9fd5-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b9fd5-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b9fd5-130">Nowe — AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b9fd5-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b9fd5-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b9fd5-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

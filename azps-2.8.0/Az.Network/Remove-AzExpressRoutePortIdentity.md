---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c7ffb86fa56a09fb0c5bbdd41e62bf8d47bee140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869715"
---
# <span data-ttu-id="7ab92-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ab92-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="7ab92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ab92-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab92-103">Usuwa tożsamość z ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7ab92-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="7ab92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ab92-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ab92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ab92-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab92-106">Polecenie cmdlet **Remove-AzExpressRoutePortIdentity** usuwa tożsamość z lokalnego obiektu usługi Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7ab92-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="7ab92-107">Użyj narzędzia **Remove-AzExpressRoutePort** , aby usunąć go z usługi ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="7ab92-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="7ab92-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ab92-108">EXAMPLES</span></span>

### <span data-ttu-id="7ab92-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7ab92-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="7ab92-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ab92-110">PARAMETERS</span></span>

### <span data-ttu-id="7ab92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab92-111">-DefaultProfile</span></span>
<span data-ttu-id="7ab92-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab92-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ab92-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ab92-113">-ExpressRoutePort</span></span>
<span data-ttu-id="7ab92-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ab92-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="7ab92-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ab92-115">-Confirm</span></span>
<span data-ttu-id="7ab92-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ab92-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab92-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab92-117">-WhatIf</span></span>
<span data-ttu-id="7ab92-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ab92-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ab92-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ab92-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab92-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab92-120">CommonParameters</span></span>
<span data-ttu-id="7ab92-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab92-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab92-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab92-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="7ab92-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ab92-123">INPUTS</span></span>

### <span data-ttu-id="7ab92-124">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ab92-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7ab92-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ab92-125">OUTPUTS</span></span>

### <span data-ttu-id="7ab92-126">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7ab92-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="7ab92-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ab92-127">NOTES</span></span>

## <span data-ttu-id="7ab92-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ab92-128">RELATED LINKS</span></span>
[<span data-ttu-id="7ab92-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ab92-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7ab92-130">Nowe — AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ab92-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="7ab92-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="7ab92-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

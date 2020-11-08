---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050295"
---
# <span data-ttu-id="d97a2-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="d97a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d97a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d97a2-103">Modyfikuje ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d97a2-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="d97a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d97a2-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d97a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d97a2-105">DESCRIPTION</span></span>
<span data-ttu-id="d97a2-106">Polecenie cmdlet **Set-AzExpressRoutePort** zapisuje zmodyfikowane ExpressRoutePort na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d97a2-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="d97a2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d97a2-107">EXAMPLES</span></span>

### <span data-ttu-id="d97a2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d97a2-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="d97a2-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d97a2-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="d97a2-110">Modyfikuje stan administratora linku ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="d97a2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d97a2-111">PARAMETERS</span></span>

### <span data-ttu-id="d97a2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d97a2-112">-AsJob</span></span>
<span data-ttu-id="d97a2-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d97a2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d97a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97a2-114">-DefaultProfile</span></span>
<span data-ttu-id="d97a2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d97a2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d97a2-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-116">-ExpressRoutePort</span></span>
<span data-ttu-id="d97a2-117">Obiekt ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d97a2-117">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d97a2-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d97a2-118">-Confirm</span></span>
<span data-ttu-id="d97a2-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d97a2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d97a2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d97a2-120">-WhatIf</span></span>
<span data-ttu-id="d97a2-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d97a2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d97a2-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d97a2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d97a2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97a2-123">CommonParameters</span></span>
<span data-ttu-id="d97a2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97a2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97a2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d97a2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97a2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d97a2-126">INPUTS</span></span>

### <span data-ttu-id="d97a2-127">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d97a2-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d97a2-128">OUTPUTS</span></span>

### <span data-ttu-id="d97a2-129">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d97a2-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d97a2-130">NOTES</span></span>

## <span data-ttu-id="d97a2-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d97a2-131">RELATED LINKS</span></span>

[<span data-ttu-id="d97a2-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="d97a2-133">Nowe — AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="d97a2-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d97a2-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

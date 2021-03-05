---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963978"
---
# <span data-ttu-id="70cc0-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="70cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="70cc0-103">Modyfikuje port expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="70cc0-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="70cc0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70cc0-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70cc0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="70cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="70cc0-106">Polecenie **cmdlet Set-AzExpressRoutePort** zapisuje zmodyfikowany port ExpressRoutePort na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="70cc0-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="70cc0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="70cc0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70cc0-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="70cc0-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="70cc0-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="70cc0-110">Modyfikuje stan administratora łącza do usługi ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="70cc0-111">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="70cc0-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="70cc0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70cc0-112">PARAMETERS</span></span>

### <span data-ttu-id="70cc0-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="70cc0-113">-AsJob</span></span>
<span data-ttu-id="70cc0-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="70cc0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70cc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70cc0-115">-DefaultProfile</span></span>
<span data-ttu-id="70cc0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="70cc0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70cc0-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-117">-ExpressRoutePort</span></span>
<span data-ttu-id="70cc0-118">Obiekt ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="70cc0-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="70cc0-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70cc0-119">-Confirm</span></span>
<span data-ttu-id="70cc0-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="70cc0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70cc0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70cc0-121">-WhatIf</span></span>
<span data-ttu-id="70cc0-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70cc0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70cc0-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="70cc0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70cc0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70cc0-124">CommonParameters</span></span>
<span data-ttu-id="70cc0-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70cc0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70cc0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70cc0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70cc0-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70cc0-127">INPUTS</span></span>

### <span data-ttu-id="70cc0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="70cc0-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70cc0-129">OUTPUTS</span></span>

### <span data-ttu-id="70cc0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="70cc0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70cc0-131">NOTES</span></span>

## <span data-ttu-id="70cc0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70cc0-132">RELATED LINKS</span></span>

[<span data-ttu-id="70cc0-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="70cc0-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="70cc0-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="70cc0-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

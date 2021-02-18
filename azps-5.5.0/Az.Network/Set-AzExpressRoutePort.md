---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: 2365729f3960e3652e2b4c0709ca14092fea3264
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240586"
---
# <span data-ttu-id="05ff4-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="05ff4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="05ff4-103">Modyfikuje port expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="05ff4-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="05ff4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05ff4-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ff4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="05ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="05ff4-106">Polecenie **cmdlet Set-AzExpressRoutePort** zapisuje zmodyfikowaną usługę ExpressRoutePort na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="05ff4-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="05ff4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="05ff4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05ff4-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="05ff4-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="05ff4-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="05ff4-110">Modyfikuje stan administratora łącza do usługi ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="05ff4-111">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="05ff4-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="05ff4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05ff4-112">PARAMETERS</span></span>

### <span data-ttu-id="05ff4-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="05ff4-113">-AsJob</span></span>
<span data-ttu-id="05ff4-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="05ff4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05ff4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ff4-115">-DefaultProfile</span></span>
<span data-ttu-id="05ff4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="05ff4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05ff4-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-117">-ExpressRoutePort</span></span>
<span data-ttu-id="05ff4-118">Obiekt ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="05ff4-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="05ff4-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05ff4-119">-Confirm</span></span>
<span data-ttu-id="05ff4-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="05ff4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ff4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ff4-121">-WhatIf</span></span>
<span data-ttu-id="05ff4-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ff4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ff4-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="05ff4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ff4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ff4-124">CommonParameters</span></span>
<span data-ttu-id="05ff4-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ff4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ff4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ff4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ff4-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05ff4-127">INPUTS</span></span>

### <span data-ttu-id="05ff4-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="05ff4-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05ff4-129">OUTPUTS</span></span>

### <span data-ttu-id="05ff4-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="05ff4-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05ff4-131">NOTES</span></span>

## <span data-ttu-id="05ff4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05ff4-132">RELATED LINKS</span></span>

[<span data-ttu-id="05ff4-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="05ff4-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="05ff4-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="05ff4-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

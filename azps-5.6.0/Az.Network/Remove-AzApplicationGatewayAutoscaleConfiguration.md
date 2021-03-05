---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e6321125958b872d15f60bbe433819c4c6f1d7ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015018"
---
# <span data-ttu-id="6ad1d-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ad1d-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6ad1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad1d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad1d-103">Usuwa konfigurację automatycznego skalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="6ad1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ad1d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad1d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ad1d-105">DESCRIPTION</span></span>
<span data-ttu-id="6ad1d-106">Polecenie **cmdlet Remove-AzApplicationGatewayAutoscaleConfiguration** usuwa konfigurację skalowania automatycznego z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="6ad1d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ad1d-107">EXAMPLES</span></span>

### <span data-ttu-id="6ad1d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ad1d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="6ad1d-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje ją w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="6ad1d-110">Drugie polecenie usuwa konfigurację automatycznego skalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="6ad1d-111">Trzecie polecenie aktualizuje bramę aplikacji na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="6ad1d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ad1d-112">PARAMETERS</span></span>

### <span data-ttu-id="6ad1d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ad1d-113">-ApplicationGateway</span></span>
<span data-ttu-id="6ad1d-114">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ad1d-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad1d-115">-DefaultProfile</span></span>
<span data-ttu-id="6ad1d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad1d-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6ad1d-117">-Force</span></span>
<span data-ttu-id="6ad1d-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6ad1d-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ad1d-119">-Confirm</span></span>
<span data-ttu-id="6ad1d-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad1d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad1d-121">-WhatIf</span></span>
<span data-ttu-id="6ad1d-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad1d-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad1d-124">CommonParameters</span></span>
<span data-ttu-id="6ad1d-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad1d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad1d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad1d-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ad1d-127">INPUTS</span></span>

### <span data-ttu-id="6ad1d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ad1d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ad1d-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ad1d-129">OUTPUTS</span></span>

### <span data-ttu-id="6ad1d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ad1d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ad1d-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ad1d-131">NOTES</span></span>

## <span data-ttu-id="6ad1d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ad1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="6ad1d-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ad1d-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6ad1d-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ad1d-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6ad1d-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ad1d-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 31b9bd5e0db4f4fd17808ea46f1f3a3d6476c5e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869791"
---
# <span data-ttu-id="ae3a4-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae3a4-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ae3a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3a4-103">Usuwa konfigurację autoskalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="ae3a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae3a4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae3a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae3a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ae3a4-106">Polecenie cmdlet **Remove-AzApplicationGatewayAutoscaleConfiguration** usuwa konfigurację skalowania automatycznego z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="ae3a4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae3a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ae3a4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae3a4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="ae3a4-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="ae3a4-110">Drugie polecenie usuwa konfigurację autoskalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="ae3a4-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="ae3a4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae3a4-112">PARAMETERS</span></span>

### <span data-ttu-id="ae3a4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae3a4-113">-ApplicationGateway</span></span>
<span data-ttu-id="ae3a4-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae3a4-114">The applicationGateway</span></span>

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

### <span data-ttu-id="ae3a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3a4-115">-DefaultProfile</span></span>
<span data-ttu-id="ae3a4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae3a4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ae3a4-117">-Force</span></span>
<span data-ttu-id="ae3a4-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ae3a4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae3a4-119">-Confirm</span></span>
<span data-ttu-id="ae3a4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae3a4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3a4-121">-WhatIf</span></span>
<span data-ttu-id="ae3a4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae3a4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae3a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3a4-124">CommonParameters</span></span>
<span data-ttu-id="ae3a4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae3a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3a4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3a4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3a4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae3a4-127">INPUTS</span></span>

### <span data-ttu-id="ae3a4-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae3a4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae3a4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae3a4-129">OUTPUTS</span></span>

### <span data-ttu-id="ae3a4-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae3a4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae3a4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae3a4-131">NOTES</span></span>

## <span data-ttu-id="ae3a4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae3a4-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae3a4-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae3a4-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ae3a4-134">Nowe — AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae3a4-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ae3a4-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae3a4-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)

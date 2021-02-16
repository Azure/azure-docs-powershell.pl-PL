---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179387"
---
# <span data-ttu-id="c9f6b-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9f6b-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c9f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f6b-103">Aktualizuje konfigurację skalowania automatycznego bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="c9f6b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9f6b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f6b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="c9f6b-106">Polecenie **cmdlet Set-AzApplicationGatewayAutoscaleConfiguration** modyfikuje istniejącą konfigurację skalowania automatycznego bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="c9f6b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="c9f6b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9f6b-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c9f6b-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje ją w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c9f6b-110">Drugie polecenie aktualizuje konfigurację automatycznego skalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="c9f6b-111">Trzecie polecenie aktualizuje bramę aplikacji na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c9f6b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9f6b-112">PARAMETERS</span></span>

### <span data-ttu-id="c9f6b-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9f6b-113">-ApplicationGateway</span></span>
<span data-ttu-id="c9f6b-114">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9f6b-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c9f6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f6b-115">-DefaultProfile</span></span>
<span data-ttu-id="c9f6b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f6b-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="c9f6b-117">-MaxCapacity</span></span>
<span data-ttu-id="c9f6b-118">Maksymalna pojemność bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f6b-119">—MinCapacity</span><span class="sxs-lookup"><span data-stu-id="c9f6b-119">-MinCapacity</span></span>
<span data-ttu-id="c9f6b-120">Minimalna pojemność bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f6b-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9f6b-121">-Confirm</span></span>
<span data-ttu-id="c9f6b-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f6b-123">-WhatIf</span></span>
<span data-ttu-id="c9f6b-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9f6b-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f6b-126">CommonParameters</span></span>
<span data-ttu-id="c9f6b-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f6b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f6b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f6b-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9f6b-129">INPUTS</span></span>

### <span data-ttu-id="c9f6b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9f6b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9f6b-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9f6b-131">OUTPUTS</span></span>

### <span data-ttu-id="c9f6b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c9f6b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c9f6b-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9f6b-133">NOTES</span></span>

## <span data-ttu-id="c9f6b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9f6b-134">RELATED LINKS</span></span>

[<span data-ttu-id="c9f6b-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9f6b-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c9f6b-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9f6b-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c9f6b-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9f6b-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

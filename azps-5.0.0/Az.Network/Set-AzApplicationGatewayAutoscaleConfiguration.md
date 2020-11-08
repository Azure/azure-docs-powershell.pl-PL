---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232768"
---
# <span data-ttu-id="45568-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="45568-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="45568-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45568-102">SYNOPSIS</span></span>
<span data-ttu-id="45568-103">Umożliwia zaktualizowanie konfiguracji autoskalowania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="45568-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="45568-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45568-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45568-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45568-105">DESCRIPTION</span></span>
<span data-ttu-id="45568-106">Polecenie cmdlet **Set-AzApplicationGatewayAutoscaleConfiguration** modyfikuje istniejącą konfigurację autoskalowania bramy Application.</span><span class="sxs-lookup"><span data-stu-id="45568-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="45568-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45568-107">EXAMPLES</span></span>

### <span data-ttu-id="45568-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45568-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="45568-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="45568-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="45568-110">Drugie polecenie aktualizuje konfigurację autoskalowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="45568-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="45568-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="45568-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="45568-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45568-112">PARAMETERS</span></span>

### <span data-ttu-id="45568-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45568-113">-ApplicationGateway</span></span>
<span data-ttu-id="45568-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45568-114">The applicationGateway</span></span>

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

### <span data-ttu-id="45568-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45568-115">-DefaultProfile</span></span>
<span data-ttu-id="45568-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45568-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45568-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="45568-117">-MaxCapacity</span></span>
<span data-ttu-id="45568-118">Maksymalna pojemność bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="45568-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="45568-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="45568-119">-MinCapacity</span></span>
<span data-ttu-id="45568-120">Minimalna pojemność bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="45568-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="45568-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45568-121">-Confirm</span></span>
<span data-ttu-id="45568-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45568-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45568-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45568-123">-WhatIf</span></span>
<span data-ttu-id="45568-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45568-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45568-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45568-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45568-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45568-126">CommonParameters</span></span>
<span data-ttu-id="45568-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45568-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45568-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45568-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45568-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45568-129">INPUTS</span></span>

### <span data-ttu-id="45568-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45568-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="45568-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45568-131">OUTPUTS</span></span>

### <span data-ttu-id="45568-132">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45568-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="45568-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45568-133">NOTES</span></span>

## <span data-ttu-id="45568-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45568-134">RELATED LINKS</span></span>

[<span data-ttu-id="45568-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="45568-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="45568-136">Nowe — AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="45568-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="45568-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="45568-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179555"
---
# <span data-ttu-id="5cab8-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cab8-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="5cab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cab8-102">SYNOPSIS</span></span>
<span data-ttu-id="5cab8-103">Usuwa konfigurację automatycznego skalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cab8-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="5cab8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5cab8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cab8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5cab8-105">DESCRIPTION</span></span>
<span data-ttu-id="5cab8-106">Polecenie **cmdlet Remove-AzApplicationGatewayAutoscaleConfiguration** usuwa konfigurację skalowania automatycznego z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cab8-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="5cab8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5cab8-107">EXAMPLES</span></span>

### <span data-ttu-id="5cab8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5cab8-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="5cab8-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje ją w $gw zmienną.</span><span class="sxs-lookup"><span data-stu-id="5cab8-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="5cab8-110">Drugie polecenie usuwa konfigurację automatycznego skalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5cab8-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="5cab8-111">Trzecie polecenie aktualizuje bramę aplikacji na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5cab8-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="5cab8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cab8-112">PARAMETERS</span></span>

### <span data-ttu-id="5cab8-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cab8-113">-ApplicationGateway</span></span>
<span data-ttu-id="5cab8-114">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cab8-114">The applicationGateway</span></span>

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

### <span data-ttu-id="5cab8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cab8-115">-DefaultProfile</span></span>
<span data-ttu-id="5cab8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cab8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cab8-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5cab8-117">-Force</span></span>
<span data-ttu-id="5cab8-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5cab8-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5cab8-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cab8-119">-Confirm</span></span>
<span data-ttu-id="5cab8-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5cab8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cab8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cab8-121">-WhatIf</span></span>
<span data-ttu-id="5cab8-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cab8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cab8-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5cab8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cab8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cab8-124">CommonParameters</span></span>
<span data-ttu-id="5cab8-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cab8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cab8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cab8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cab8-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cab8-127">INPUTS</span></span>

### <span data-ttu-id="5cab8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cab8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5cab8-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cab8-129">OUTPUTS</span></span>

### <span data-ttu-id="5cab8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cab8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5cab8-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5cab8-131">NOTES</span></span>

## <span data-ttu-id="5cab8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cab8-132">RELATED LINKS</span></span>

[<span data-ttu-id="5cab8-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cab8-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5cab8-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cab8-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5cab8-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5cab8-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)

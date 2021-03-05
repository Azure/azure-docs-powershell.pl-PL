---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: e5ac68f10a75dff94313fa17830720466e82da5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990977"
---
# <span data-ttu-id="7ac43-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ac43-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="7ac43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ac43-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac43-103">Usuwa zasady SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac43-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="7ac43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ac43-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ac43-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ac43-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac43-106">Polecenie Remove-AzApplicationGatewaySslPolicy cmdlet usuwa zasady SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac43-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="7ac43-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ac43-107">EXAMPLES</span></span>

### <span data-ttu-id="7ac43-108">Przykład 1. Usuwanie zasad SSL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7ac43-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="7ac43-109">To polecenie usuwa zasady SSL z bramy aplikacji o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="7ac43-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="7ac43-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ac43-110">PARAMETERS</span></span>

### <span data-ttu-id="7ac43-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ac43-111">-ApplicationGateway</span></span>
<span data-ttu-id="7ac43-112">Określa bramę aplikacji, z której to polecenie cmdlet usuwa zasady SSL.</span><span class="sxs-lookup"><span data-stu-id="7ac43-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="7ac43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac43-113">-DefaultProfile</span></span>
<span data-ttu-id="7ac43-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac43-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7ac43-115">-Force</span></span>
<span data-ttu-id="7ac43-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ac43-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7ac43-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ac43-117">-Confirm</span></span>
<span data-ttu-id="7ac43-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ac43-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac43-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac43-119">-WhatIf</span></span>
<span data-ttu-id="7ac43-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac43-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac43-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7ac43-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac43-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac43-122">CommonParameters</span></span>
<span data-ttu-id="7ac43-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac43-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac43-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac43-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac43-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac43-125">INPUTS</span></span>

### <span data-ttu-id="7ac43-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ac43-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ac43-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ac43-127">OUTPUTS</span></span>

### <span data-ttu-id="7ac43-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ac43-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ac43-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ac43-129">NOTES</span></span>
<span data-ttu-id="7ac43-130">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="7ac43-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7ac43-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ac43-131">RELATED LINKS</span></span>

[<span data-ttu-id="7ac43-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ac43-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="7ac43-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ac43-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="7ac43-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="7ac43-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)


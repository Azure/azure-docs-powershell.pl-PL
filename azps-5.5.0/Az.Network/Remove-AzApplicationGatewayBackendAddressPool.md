---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240722"
---
# <span data-ttu-id="7977c-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7977c-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7977c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7977c-102">SYNOPSIS</span></span>
<span data-ttu-id="7977c-103">Usuwa pulę adresów z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7977c-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="7977c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7977c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7977c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7977c-105">DESCRIPTION</span></span>
<span data-ttu-id="7977c-106">Polecenie **cmdlet Remove-AzApplicationGatewayBackendAddressPool** usuwa pulę adresów zaplecza z bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="7977c-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="7977c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7977c-107">EXAMPLES</span></span>

### <span data-ttu-id="7977c-108">Przykład 1. Usuwanie puli adresów back-end z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7977c-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="7977c-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 należącą do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="7977c-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="7977c-110">Drugie polecenie usuwa z bramy aplikacji pulę adresów zaplecza o nazwie BackEndPool02.</span><span class="sxs-lookup"><span data-stu-id="7977c-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="7977c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7977c-111">PARAMETERS</span></span>

### <span data-ttu-id="7977c-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7977c-112">-ApplicationGateway</span></span>
<span data-ttu-id="7977c-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa pulę adresów back-end.</span><span class="sxs-lookup"><span data-stu-id="7977c-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="7977c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7977c-114">-DefaultProfile</span></span>
<span data-ttu-id="7977c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7977c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7977c-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7977c-116">-Name</span></span>
<span data-ttu-id="7977c-117">Określa nazwę puli adresów back-end, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7977c-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7977c-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7977c-118">-Confirm</span></span>
<span data-ttu-id="7977c-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7977c-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7977c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7977c-120">-WhatIf</span></span>
<span data-ttu-id="7977c-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7977c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7977c-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7977c-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7977c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7977c-123">CommonParameters</span></span>
<span data-ttu-id="7977c-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7977c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7977c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7977c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7977c-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7977c-126">INPUTS</span></span>

### <span data-ttu-id="7977c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7977c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7977c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7977c-128">OUTPUTS</span></span>

### <span data-ttu-id="7977c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7977c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7977c-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7977c-130">NOTES</span></span>

## <span data-ttu-id="7977c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7977c-131">RELATED LINKS</span></span>

[<span data-ttu-id="7977c-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7977c-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7977c-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7977c-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7977c-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7977c-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7977c-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7977c-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)



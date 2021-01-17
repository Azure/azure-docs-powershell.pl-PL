---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378833"
---
# <span data-ttu-id="d7915-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d7915-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d7915-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7915-102">SYNOPSIS</span></span>
<span data-ttu-id="d7915-103">Usuwa pulę adresów zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d7915-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="d7915-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7915-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7915-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7915-105">DESCRIPTION</span></span>
<span data-ttu-id="d7915-106">Polecenie cmdlet **Remove-AzApplicationGatewayBackendAddressPool** usuwa pulę adresów zaplecza z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7915-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="d7915-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7915-107">EXAMPLES</span></span>

### <span data-ttu-id="d7915-108">Przykład 1: Usuwanie puli adresów zaplecza z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d7915-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="d7915-109">Pierwsze polecenie pobiera bramkę Applications o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d7915-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="d7915-110">Drugie polecenie usuwa pulę adresów zaplecza o nazwie BackEndPool02 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d7915-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="d7915-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7915-111">PARAMETERS</span></span>

### <span data-ttu-id="d7915-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7915-112">-ApplicationGateway</span></span>
<span data-ttu-id="d7915-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d7915-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="d7915-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7915-114">-DefaultProfile</span></span>
<span data-ttu-id="d7915-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7915-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7915-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7915-116">-Name</span></span>
<span data-ttu-id="d7915-117">Określa nazwę puli adresów zaplecza, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7915-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d7915-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7915-118">-Confirm</span></span>
<span data-ttu-id="d7915-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7915-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7915-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7915-120">-WhatIf</span></span>
<span data-ttu-id="d7915-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7915-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7915-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7915-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7915-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7915-123">CommonParameters</span></span>
<span data-ttu-id="d7915-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7915-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7915-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7915-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7915-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7915-126">INPUTS</span></span>

### <span data-ttu-id="d7915-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7915-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7915-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7915-128">OUTPUTS</span></span>

### <span data-ttu-id="d7915-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d7915-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d7915-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7915-130">NOTES</span></span>

## <span data-ttu-id="d7915-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7915-131">RELATED LINKS</span></span>

[<span data-ttu-id="d7915-132">Dodaj-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d7915-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d7915-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d7915-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d7915-134">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d7915-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d7915-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d7915-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)



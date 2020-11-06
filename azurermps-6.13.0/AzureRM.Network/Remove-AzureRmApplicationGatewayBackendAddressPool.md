---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 996a2c17b6283e967eaca8462f4d703aed60d19c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543671"
---
# <span data-ttu-id="be4a3-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be4a3-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="be4a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="be4a3-103">Usuwa pulę adresów zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="be4a3-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be4a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be4a3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be4a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="be4a3-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayBackendAddressPool** usuwa pulę adresów zaplecza z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be4a3-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="be4a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="be4a3-108">Przykład 1: Usuwanie puli adresów zaplecza z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="be4a3-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="be4a3-109">Pierwsze polecenie pobiera bramkę Applications o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="be4a3-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="be4a3-110">Drugie polecenie usuwa pulę adresów zaplecza o nazwie BackEndPool02 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="be4a3-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="be4a3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be4a3-111">PARAMETERS</span></span>

### <span data-ttu-id="be4a3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be4a3-112">-ApplicationGateway</span></span>
<span data-ttu-id="be4a3-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="be4a3-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="be4a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4a3-114">-DefaultProfile</span></span>
<span data-ttu-id="be4a3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be4a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4a3-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be4a3-116">-Name</span></span>
<span data-ttu-id="be4a3-117">Określa nazwę puli adresów zaplecza, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be4a3-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be4a3-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be4a3-118">-Confirm</span></span>
<span data-ttu-id="be4a3-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be4a3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be4a3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be4a3-120">-WhatIf</span></span>
<span data-ttu-id="be4a3-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be4a3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be4a3-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="be4a3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be4a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4a3-123">CommonParameters</span></span>
<span data-ttu-id="be4a3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be4a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4a3-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be4a3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4a3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be4a3-126">INPUTS</span></span>

### <span data-ttu-id="be4a3-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="be4a3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="be4a3-128">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be4a3-128">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="be4a3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be4a3-129">OUTPUTS</span></span>

### <span data-ttu-id="be4a3-130">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be4a3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="be4a3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be4a3-131">NOTES</span></span>

## <span data-ttu-id="be4a3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be4a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="be4a3-133">Dodaj-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be4a3-133">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="be4a3-134">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be4a3-134">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="be4a3-135">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be4a3-135">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="be4a3-136">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be4a3-136">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)



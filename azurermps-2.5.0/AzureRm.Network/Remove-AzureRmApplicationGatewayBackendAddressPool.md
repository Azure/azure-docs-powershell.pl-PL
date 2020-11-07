---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 7b82cf189d912d000c143b20cca76c4f2683b7d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898700"
---
# <span data-ttu-id="fde88-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fde88-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="fde88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fde88-102">SYNOPSIS</span></span>
<span data-ttu-id="fde88-103">Usuwa pulę adresów zaplecza z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fde88-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fde88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fde88-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fde88-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fde88-105">DESCRIPTION</span></span>
<span data-ttu-id="fde88-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayBackendAddressPool** usuwa pulę adresów zaplecza z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fde88-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="fde88-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fde88-107">EXAMPLES</span></span>

### <span data-ttu-id="fde88-108">Przykład 1: Usuwanie puli adresów zaplecza z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="fde88-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="fde88-109">Pierwsze polecenie pobiera bramkę Applications o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fde88-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="fde88-110">Drugie polecenie usuwa pulę adresów zaplecza o nazwie BackEndPool02 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fde88-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="fde88-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fde88-111">PARAMETERS</span></span>

### <span data-ttu-id="fde88-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fde88-112">-ApplicationGateway</span></span>
<span data-ttu-id="fde88-113">Określa bramę aplikacji, z której to polecenie cmdlet usuwa pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="fde88-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fde88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde88-114">-DefaultProfile</span></span>
<span data-ttu-id="fde88-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fde88-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde88-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fde88-116">-Name</span></span>
<span data-ttu-id="fde88-117">Określa nazwę puli adresów zaplecza, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fde88-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde88-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fde88-118">-Confirm</span></span>
<span data-ttu-id="fde88-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fde88-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde88-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde88-120">-WhatIf</span></span>
<span data-ttu-id="fde88-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fde88-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde88-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fde88-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde88-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde88-123">CommonParameters</span></span>
<span data-ttu-id="fde88-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde88-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde88-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde88-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde88-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fde88-126">INPUTS</span></span>

### <span data-ttu-id="fde88-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fde88-127">System.String</span></span>

## <span data-ttu-id="fde88-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fde88-128">OUTPUTS</span></span>

### <span data-ttu-id="fde88-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fde88-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="fde88-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fde88-130">NOTES</span></span>

## <span data-ttu-id="fde88-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fde88-131">RELATED LINKS</span></span>

[<span data-ttu-id="fde88-132">Dodaj-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fde88-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fde88-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fde88-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fde88-134">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fde88-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fde88-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fde88-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)



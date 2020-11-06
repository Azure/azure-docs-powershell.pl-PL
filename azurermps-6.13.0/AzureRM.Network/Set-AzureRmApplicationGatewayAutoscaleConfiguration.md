---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548632"
---
# <span data-ttu-id="7f69d-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f69d-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7f69d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f69d-102">SYNOPSIS</span></span>
<span data-ttu-id="7f69d-103">Umożliwia zaktualizowanie konfiguracji autoskalowania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7f69d-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f69d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f69d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f69d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f69d-105">DESCRIPTION</span></span>
<span data-ttu-id="7f69d-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayAutoscaleConfiguration** modyfikuje istniejącą konfigurację autoskalowania bramy Application.</span><span class="sxs-lookup"><span data-stu-id="7f69d-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="7f69d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f69d-107">EXAMPLES</span></span>

### <span data-ttu-id="7f69d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f69d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="7f69d-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="7f69d-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="7f69d-110">Drugie polecenie aktualizuje konfigurację autoskalowania na bramie applicationg.</span><span class="sxs-lookup"><span data-stu-id="7f69d-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="7f69d-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7f69d-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="7f69d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f69d-112">PARAMETERS</span></span>

### <span data-ttu-id="7f69d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f69d-113">-ApplicationGateway</span></span>
<span data-ttu-id="7f69d-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f69d-114">The applicationGateway</span></span>

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

### <span data-ttu-id="7f69d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f69d-115">-DefaultProfile</span></span>
<span data-ttu-id="7f69d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f69d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f69d-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="7f69d-117">-MinCapacity</span></span>
<span data-ttu-id="7f69d-118">Minimalne capcity dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f69d-118">Minimum capcity for application gateway.</span></span>

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

### <span data-ttu-id="7f69d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f69d-119">-Confirm</span></span>
<span data-ttu-id="7f69d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f69d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f69d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f69d-121">-WhatIf</span></span>
<span data-ttu-id="7f69d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f69d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f69d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f69d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f69d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f69d-124">CommonParameters</span></span>
<span data-ttu-id="7f69d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f69d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f69d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f69d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f69d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f69d-127">INPUTS</span></span>

### <span data-ttu-id="7f69d-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f69d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f69d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f69d-129">OUTPUTS</span></span>

### <span data-ttu-id="7f69d-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f69d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f69d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f69d-131">NOTES</span></span>

## <span data-ttu-id="7f69d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f69d-132">RELATED LINKS</span></span>

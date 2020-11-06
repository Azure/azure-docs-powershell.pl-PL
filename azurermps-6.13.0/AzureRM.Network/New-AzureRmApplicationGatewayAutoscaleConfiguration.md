---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551172"
---
# <span data-ttu-id="84c90-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="84c90-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="84c90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84c90-102">SYNOPSIS</span></span>
<span data-ttu-id="84c90-103">Umożliwia utworzenie konfiguracji autoskalowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="84c90-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84c90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84c90-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84c90-105">DESCRIPTION</span></span>
<span data-ttu-id="84c90-106">Polecenie cmdlet **New-AzureRmApplicationGatewayAutoscaleConfiguration** umożliwia utworzenie konfiguracji autoskalowania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="84c90-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="84c90-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84c90-107">EXAMPLES</span></span>

### <span data-ttu-id="84c90-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84c90-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="84c90-109">Pierwsze polecenie powoduje utworzenie konfiguracji autoskalowania o minimalnej pojemności 3.</span><span class="sxs-lookup"><span data-stu-id="84c90-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="84c90-110">Drugie polecenie tworzy bramę aplikacji z konfiguracją skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="84c90-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="84c90-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84c90-111">PARAMETERS</span></span>

### <span data-ttu-id="84c90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c90-112">-DefaultProfile</span></span>
<span data-ttu-id="84c90-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84c90-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c90-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="84c90-114">-MinCapacity</span></span>
<span data-ttu-id="84c90-115">Minimalne jednostki wydajności, które zawsze będą dostępne [i naliczone] dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="84c90-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="84c90-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84c90-116">-Confirm</span></span>
<span data-ttu-id="84c90-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c90-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c90-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c90-118">-WhatIf</span></span>
<span data-ttu-id="84c90-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c90-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c90-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84c90-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c90-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c90-121">CommonParameters</span></span>
<span data-ttu-id="84c90-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c90-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c90-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84c90-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c90-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84c90-124">INPUTS</span></span>

### <span data-ttu-id="84c90-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="84c90-125">None</span></span>

## <span data-ttu-id="84c90-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84c90-126">OUTPUTS</span></span>

### <span data-ttu-id="84c90-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="84c90-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="84c90-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84c90-128">NOTES</span></span>

## <span data-ttu-id="84c90-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84c90-129">RELATED LINKS</span></span>

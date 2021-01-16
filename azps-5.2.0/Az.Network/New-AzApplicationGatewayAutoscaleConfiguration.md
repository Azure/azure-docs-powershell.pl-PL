---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361048"
---
# <span data-ttu-id="f333f-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f333f-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f333f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f333f-102">SYNOPSIS</span></span>
<span data-ttu-id="f333f-103">Umożliwia utworzenie konfiguracji autoskalowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f333f-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="f333f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f333f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f333f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f333f-105">DESCRIPTION</span></span>
<span data-ttu-id="f333f-106">Polecenie cmdlet **New-AzApplicationGatewayAutoscaleConfiguration** umożliwia utworzenie konfiguracji autoskalowania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f333f-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="f333f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f333f-107">EXAMPLES</span></span>

### <span data-ttu-id="f333f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f333f-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="f333f-109">Pierwsze polecenie powoduje utworzenie konfiguracji autoskalowania o minimalnej pojemności 3.</span><span class="sxs-lookup"><span data-stu-id="f333f-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="f333f-110">Drugie polecenie tworzy bramę aplikacji z konfiguracją skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="f333f-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="f333f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f333f-111">PARAMETERS</span></span>

### <span data-ttu-id="f333f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f333f-112">-DefaultProfile</span></span>
<span data-ttu-id="f333f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f333f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f333f-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="f333f-114">-MaxCapacity</span></span>
<span data-ttu-id="f333f-115">Maksymalna liczba jednostek wydajności, które zawsze są dostępne [i naliczone] dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f333f-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="f333f-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="f333f-116">-MinCapacity</span></span>
<span data-ttu-id="f333f-117">Minimalne jednostki wydajności, które zawsze będą dostępne [i naliczone] dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f333f-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="f333f-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f333f-118">-Confirm</span></span>
<span data-ttu-id="f333f-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f333f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f333f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f333f-120">-WhatIf</span></span>
<span data-ttu-id="f333f-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f333f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f333f-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f333f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f333f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f333f-123">CommonParameters</span></span>
<span data-ttu-id="f333f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f333f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f333f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f333f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f333f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f333f-126">INPUTS</span></span>

### <span data-ttu-id="f333f-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f333f-127">None</span></span>

## <span data-ttu-id="f333f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f333f-128">OUTPUTS</span></span>

### <span data-ttu-id="f333f-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f333f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f333f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f333f-130">NOTES</span></span>

## <span data-ttu-id="f333f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f333f-131">RELATED LINKS</span></span>

[<span data-ttu-id="f333f-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f333f-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f333f-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f333f-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f333f-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f333f-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)

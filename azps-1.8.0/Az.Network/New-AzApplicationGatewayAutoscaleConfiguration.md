---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 0d99ec672d75844eca37cb63d63a2c6d7433d04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709397"
---
# <span data-ttu-id="ea192-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea192-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ea192-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea192-102">SYNOPSIS</span></span>
<span data-ttu-id="ea192-103">Umożliwia utworzenie konfiguracji autoskalowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ea192-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="ea192-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea192-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea192-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea192-105">DESCRIPTION</span></span>
<span data-ttu-id="ea192-106">Polecenie cmdlet **New-AzApplicationGatewayAutoscaleConfiguration** umożliwia utworzenie konfiguracji autoskalowania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ea192-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="ea192-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea192-107">EXAMPLES</span></span>

### <span data-ttu-id="ea192-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ea192-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="ea192-109">Pierwsze polecenie powoduje utworzenie konfiguracji autoskalowania o minimalnej pojemności 3.</span><span class="sxs-lookup"><span data-stu-id="ea192-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="ea192-110">Drugie polecenie tworzy bramę aplikacji z konfiguracją skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="ea192-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="ea192-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea192-111">PARAMETERS</span></span>

### <span data-ttu-id="ea192-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea192-112">-DefaultProfile</span></span>
<span data-ttu-id="ea192-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea192-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea192-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="ea192-114">-MaxCapacity</span></span>
<span data-ttu-id="ea192-115">Maksymalna liczba jednostek wydajności, które zawsze są dostępne [i naliczone] dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea192-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="ea192-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="ea192-116">-MinCapacity</span></span>
<span data-ttu-id="ea192-117">Minimalne jednostki wydajności, które zawsze będą dostępne [i naliczone] dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ea192-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="ea192-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea192-118">-Confirm</span></span>
<span data-ttu-id="ea192-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea192-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea192-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea192-120">-WhatIf</span></span>
<span data-ttu-id="ea192-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea192-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea192-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea192-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea192-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea192-123">CommonParameters</span></span>
<span data-ttu-id="ea192-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea192-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea192-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea192-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea192-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea192-126">INPUTS</span></span>

### <span data-ttu-id="ea192-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ea192-127">None</span></span>

## <span data-ttu-id="ea192-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea192-128">OUTPUTS</span></span>

### <span data-ttu-id="ea192-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea192-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ea192-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea192-130">NOTES</span></span>

## <span data-ttu-id="ea192-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea192-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea192-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea192-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ea192-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea192-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ea192-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea192-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240923"
---
# <span data-ttu-id="e04ef-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e04ef-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="e04ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e04ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e04ef-103">Tworzy konfigurację automatycznego skalowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e04ef-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="e04ef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e04ef-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e04ef-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e04ef-105">DESCRIPTION</span></span>
<span data-ttu-id="e04ef-106">Polecenie **cmdlet New-AzApplicationGatewayAutoscaleConfiguration** tworzy konfigurację autoskalowania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e04ef-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="e04ef-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e04ef-107">EXAMPLES</span></span>

### <span data-ttu-id="e04ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e04ef-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="e04ef-109">Pierwsze polecenie tworzy konfigurację skalowania automatycznego o minimalnej pojemności 3.</span><span class="sxs-lookup"><span data-stu-id="e04ef-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="e04ef-110">Drugie polecenie tworzy bramę aplikacji z konfiguracją skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="e04ef-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="e04ef-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e04ef-111">PARAMETERS</span></span>

### <span data-ttu-id="e04ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04ef-112">-DefaultProfile</span></span>
<span data-ttu-id="e04ef-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e04ef-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e04ef-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="e04ef-114">-MaxCapacity</span></span>
<span data-ttu-id="e04ef-115">Maksymalna liczba jednostek pojemności, które będą zawsze dostępne dla bramy aplikacji (i pobierana opłata).</span><span class="sxs-lookup"><span data-stu-id="e04ef-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="e04ef-116">—MinCapacity</span><span class="sxs-lookup"><span data-stu-id="e04ef-116">-MinCapacity</span></span>
<span data-ttu-id="e04ef-117">Jednostki minimalnej pojemności, które będą zawsze dostępne dla bramy aplikacji (i obciążone opłatami).</span><span class="sxs-lookup"><span data-stu-id="e04ef-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="e04ef-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e04ef-118">-Confirm</span></span>
<span data-ttu-id="e04ef-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e04ef-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e04ef-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04ef-120">-WhatIf</span></span>
<span data-ttu-id="e04ef-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04ef-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e04ef-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e04ef-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e04ef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04ef-123">CommonParameters</span></span>
<span data-ttu-id="e04ef-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e04ef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04ef-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04ef-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04ef-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e04ef-126">INPUTS</span></span>

### <span data-ttu-id="e04ef-127">Brak</span><span class="sxs-lookup"><span data-stu-id="e04ef-127">None</span></span>

## <span data-ttu-id="e04ef-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e04ef-128">OUTPUTS</span></span>

### <span data-ttu-id="e04ef-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e04ef-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="e04ef-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e04ef-130">NOTES</span></span>

## <span data-ttu-id="e04ef-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e04ef-131">RELATED LINKS</span></span>

[<span data-ttu-id="e04ef-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e04ef-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="e04ef-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e04ef-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="e04ef-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e04ef-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)

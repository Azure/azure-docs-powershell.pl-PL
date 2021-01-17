---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353401"
---
# <span data-ttu-id="14468-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="14468-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="14468-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14468-102">SYNOPSIS</span></span>
<span data-ttu-id="14468-103">Aktualizowanie istniejącego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="14468-103">update an existing application insights resource</span></span>

## <span data-ttu-id="14468-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14468-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14468-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14468-105">DESCRIPTION</span></span>
<span data-ttu-id="14468-106">Aktualizowanie istniejącego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="14468-106">update an existing application insights resource</span></span>

## <span data-ttu-id="14468-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14468-107">EXAMPLES</span></span>

### <span data-ttu-id="14468-108">Przykład 1 aktualizacja składnika Application Insights</span><span class="sxs-lookup"><span data-stu-id="14468-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="14468-109">aktualizowanie składnika Application Insights "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery na "Disabled"</span><span class="sxs-lookup"><span data-stu-id="14468-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="14468-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14468-110">PARAMETERS</span></span>

### <span data-ttu-id="14468-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14468-111">-DefaultProfile</span></span>
<span data-ttu-id="14468-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14468-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14468-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14468-113">-Name</span></span>
<span data-ttu-id="14468-114">Nazwa zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="14468-114">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14468-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="14468-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="14468-116">Typ dostępu do sieci służący do uzyskiwania dostępu do pokarmowania w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="14468-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="14468-117">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="14468-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14468-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="14468-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="14468-119">Typ dostępu do sieci służący do uzyskiwania dostępu do zapytania usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="14468-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="14468-120">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="14468-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14468-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14468-121">-ResourceGroupName</span></span>
<span data-ttu-id="14468-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14468-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14468-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="14468-123">-RetentionInDays</span></span>
<span data-ttu-id="14468-124">Utrzymanie jest domyślnie zachowywane w dniach 90.</span><span class="sxs-lookup"><span data-stu-id="14468-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14468-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="14468-125">-Tag</span></span>
<span data-ttu-id="14468-126">Znaczniki składników.</span><span class="sxs-lookup"><span data-stu-id="14468-126">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14468-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14468-127">-Confirm</span></span>
<span data-ttu-id="14468-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14468-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14468-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14468-129">-WhatIf</span></span>
<span data-ttu-id="14468-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14468-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14468-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="14468-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14468-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14468-132">CommonParameters</span></span>
<span data-ttu-id="14468-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14468-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14468-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14468-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14468-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14468-135">INPUTS</span></span>

### <span data-ttu-id="14468-136">System. String</span><span class="sxs-lookup"><span data-stu-id="14468-136">System.String</span></span>

## <span data-ttu-id="14468-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14468-137">OUTPUTS</span></span>

### <span data-ttu-id="14468-138">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="14468-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="14468-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14468-139">NOTES</span></span>

## <span data-ttu-id="14468-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14468-140">RELATED LINKS</span></span>

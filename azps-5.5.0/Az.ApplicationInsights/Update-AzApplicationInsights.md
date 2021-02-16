---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244299"
---
# <span data-ttu-id="50469-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="50469-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="50469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50469-102">SYNOPSIS</span></span>
<span data-ttu-id="50469-103">aktualizowanie istniejącego zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="50469-103">update an existing application insights resource</span></span>

## <span data-ttu-id="50469-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50469-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50469-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="50469-105">DESCRIPTION</span></span>
<span data-ttu-id="50469-106">aktualizowanie istniejącego zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="50469-106">update an existing application insights resource</span></span>

## <span data-ttu-id="50469-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50469-107">EXAMPLES</span></span>

### <span data-ttu-id="50469-108">Przykład 1. Aktualizowanie składnika szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="50469-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="50469-109">aktualizowanie składnika "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery do wartości "Disabled"</span><span class="sxs-lookup"><span data-stu-id="50469-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="50469-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50469-110">PARAMETERS</span></span>

### <span data-ttu-id="50469-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50469-111">-DefaultProfile</span></span>
<span data-ttu-id="50469-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="50469-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50469-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50469-113">-Name</span></span>
<span data-ttu-id="50469-114">Nazwa zasobu szczegółowych informacji o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50469-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="50469-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="50469-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="50469-116">Typ dostępu sieciowego do uzyskiwania dostępu do aplikacji Insights ingestion.</span><span class="sxs-lookup"><span data-stu-id="50469-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="50469-117">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="50469-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="50469-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="50469-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="50469-119">Typ dostępu sieciowego do uzyskiwania dostępu do zapytania szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50469-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="50469-120">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="50469-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="50469-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50469-121">-ResourceGroupName</span></span>
<span data-ttu-id="50469-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50469-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="50469-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="50469-123">-RetentionInDays</span></span>
<span data-ttu-id="50469-124">Domyślnie przechowywanie w dniach wynosi 90 dni.</span><span class="sxs-lookup"><span data-stu-id="50469-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="50469-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="50469-125">-Tag</span></span>
<span data-ttu-id="50469-126">Tagi składników.</span><span class="sxs-lookup"><span data-stu-id="50469-126">Component Tags.</span></span>

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

### <span data-ttu-id="50469-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50469-127">-Confirm</span></span>
<span data-ttu-id="50469-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50469-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50469-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50469-129">-WhatIf</span></span>
<span data-ttu-id="50469-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50469-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50469-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50469-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50469-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50469-132">CommonParameters</span></span>
<span data-ttu-id="50469-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50469-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50469-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50469-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50469-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50469-135">INPUTS</span></span>

### <span data-ttu-id="50469-136">System.String</span><span class="sxs-lookup"><span data-stu-id="50469-136">System.String</span></span>

## <span data-ttu-id="50469-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50469-137">OUTPUTS</span></span>

### <span data-ttu-id="50469-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="50469-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="50469-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50469-139">NOTES</span></span>

## <span data-ttu-id="50469-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50469-140">RELATED LINKS</span></span>

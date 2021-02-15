---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182283"
---
# <span data-ttu-id="dce76-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="dce76-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="dce76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dce76-102">SYNOPSIS</span></span>
<span data-ttu-id="dce76-103">Tworzenie nowego zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="dce76-103">Create a new application insights resource</span></span>

## <span data-ttu-id="dce76-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dce76-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dce76-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dce76-105">DESCRIPTION</span></span>
<span data-ttu-id="dce76-106">Tworzenie nowego zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="dce76-106">Create a new application insights resource</span></span>

## <span data-ttu-id="dce76-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dce76-107">EXAMPLES</span></span>

### <span data-ttu-id="dce76-108">Przykład 1. Tworzenie nowego zasobu szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="dce76-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="dce76-109">Dodawanie nowego zasobu szczegółowych informacji o nazwie "test" w grupie zasobów "grupa testowa" z rodzajem "java"</span><span class="sxs-lookup"><span data-stu-id="dce76-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="dce76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dce76-110">PARAMETERS</span></span>

### <span data-ttu-id="dce76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce76-111">-DefaultProfile</span></span>
<span data-ttu-id="dce76-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dce76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dce76-113">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="dce76-113">-Kind</span></span>
<span data-ttu-id="dce76-114">Rodzaj aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dce76-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce76-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dce76-115">-Location</span></span>
<span data-ttu-id="dce76-116">Lokalizacja zasobu szczegółowych informacji o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dce76-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce76-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dce76-117">-Name</span></span>
<span data-ttu-id="dce76-118">Nazwa zasobu szczegółowych informacji o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dce76-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="dce76-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="dce76-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="dce76-120">Typ dostępu sieciowego do uzyskiwania dostępu do aplikacji Insights ingestion.</span><span class="sxs-lookup"><span data-stu-id="dce76-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="dce76-121">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="dce76-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce76-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="dce76-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="dce76-123">Typ dostępu sieciowego do uzyskiwania dostępu do zapytania Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dce76-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="dce76-124">Wartość powinna być "Włączona" lub "Wyłączona"</span><span class="sxs-lookup"><span data-stu-id="dce76-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce76-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce76-125">-ResourceGroupName</span></span>
<span data-ttu-id="dce76-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dce76-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="dce76-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="dce76-127">-RetentionInDays</span></span>
<span data-ttu-id="dce76-128">Domyślnie przechowywanie w dniach wynosi 90 dni.</span><span class="sxs-lookup"><span data-stu-id="dce76-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce76-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="dce76-129">-Tag</span></span>
<span data-ttu-id="dce76-130">Tagi składników.</span><span class="sxs-lookup"><span data-stu-id="dce76-130">Component Tags.</span></span>

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

### <span data-ttu-id="dce76-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dce76-131">-Confirm</span></span>
<span data-ttu-id="dce76-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dce76-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce76-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce76-133">-WhatIf</span></span>
<span data-ttu-id="dce76-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dce76-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dce76-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dce76-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce76-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce76-136">CommonParameters</span></span>
<span data-ttu-id="dce76-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce76-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce76-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dce76-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce76-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dce76-139">INPUTS</span></span>

### <span data-ttu-id="dce76-140">Brak</span><span class="sxs-lookup"><span data-stu-id="dce76-140">None</span></span>

## <span data-ttu-id="dce76-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dce76-141">OUTPUTS</span></span>

### <span data-ttu-id="dce76-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="dce76-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="dce76-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dce76-143">NOTES</span></span>

## <span data-ttu-id="dce76-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dce76-144">RELATED LINKS</span></span>

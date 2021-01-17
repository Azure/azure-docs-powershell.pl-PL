---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353533"
---
# <span data-ttu-id="18055-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="18055-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="18055-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18055-102">SYNOPSIS</span></span>
<span data-ttu-id="18055-103">Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="18055-103">Create a new application insights resource</span></span>

## <span data-ttu-id="18055-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18055-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18055-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18055-105">DESCRIPTION</span></span>
<span data-ttu-id="18055-106">Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="18055-106">Create a new application insights resource</span></span>

## <span data-ttu-id="18055-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18055-107">EXAMPLES</span></span>

### <span data-ttu-id="18055-108">Przykład 1 Tworzenie nowego zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="18055-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="18055-109">Dodawanie nowego zasobu usługi Application Insights o nazwie "test" w grupie zasób "z typem" Java "</span><span class="sxs-lookup"><span data-stu-id="18055-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="18055-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18055-110">PARAMETERS</span></span>

### <span data-ttu-id="18055-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18055-111">-DefaultProfile</span></span>
<span data-ttu-id="18055-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18055-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18055-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="18055-113">-Kind</span></span>
<span data-ttu-id="18055-114">Rodzaj aplikacji.</span><span class="sxs-lookup"><span data-stu-id="18055-114">Application kind.</span></span>

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

### <span data-ttu-id="18055-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="18055-115">-Location</span></span>
<span data-ttu-id="18055-116">Lokalizacja zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="18055-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="18055-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18055-117">-Name</span></span>
<span data-ttu-id="18055-118">Nazwa zasobu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="18055-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="18055-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="18055-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="18055-120">Typ dostępu do sieci służący do uzyskiwania dostępu do pokarmowania w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="18055-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="18055-121">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="18055-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="18055-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="18055-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="18055-123">Typ dostępu do sieci służący do uzyskiwania dostępu do zapytania usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="18055-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="18055-124">Wartość powinna być równa "Enabled" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="18055-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="18055-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18055-125">-ResourceGroupName</span></span>
<span data-ttu-id="18055-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18055-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="18055-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="18055-127">-RetentionInDays</span></span>
<span data-ttu-id="18055-128">Utrzymanie jest domyślnie zachowywane w dniach 90.</span><span class="sxs-lookup"><span data-stu-id="18055-128">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="18055-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="18055-129">-Tag</span></span>
<span data-ttu-id="18055-130">Znaczniki składników.</span><span class="sxs-lookup"><span data-stu-id="18055-130">Component Tags.</span></span>

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

### <span data-ttu-id="18055-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18055-131">-Confirm</span></span>
<span data-ttu-id="18055-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18055-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18055-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18055-133">-WhatIf</span></span>
<span data-ttu-id="18055-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18055-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18055-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18055-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18055-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18055-136">CommonParameters</span></span>
<span data-ttu-id="18055-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18055-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18055-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18055-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18055-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18055-139">INPUTS</span></span>

### <span data-ttu-id="18055-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="18055-140">None</span></span>

## <span data-ttu-id="18055-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18055-141">OUTPUTS</span></span>

### <span data-ttu-id="18055-142">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="18055-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="18055-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18055-143">NOTES</span></span>

## <span data-ttu-id="18055-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18055-144">RELATED LINKS</span></span>

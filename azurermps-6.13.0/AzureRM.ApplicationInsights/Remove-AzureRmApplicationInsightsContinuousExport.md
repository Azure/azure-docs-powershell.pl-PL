---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: b9a26a1279b89609728837def1997ac5735ddaea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542015"
---
# <span data-ttu-id="a607b-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="a607b-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="a607b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a607b-102">SYNOPSIS</span></span>
<span data-ttu-id="a607b-103">Usuwanie konfiguracji eksportu cotinuous w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="a607b-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a607b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a607b-104">SYNTAX</span></span>

### <span data-ttu-id="a607b-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a607b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a607b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a607b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a607b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a607b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a607b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a607b-108">DESCRIPTION</span></span>
<span data-ttu-id="a607b-109">Usuwanie konfiguracji eksportu cotinuous w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="a607b-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="a607b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a607b-110">EXAMPLES</span></span>

### <span data-ttu-id="a607b-111">Przykład 1 Usuwanie konfiguracji eksportu cotinuous w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="a607b-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="a607b-112">Usuwanie ciągłej konfiguracji eksportu w usłudze Application Insights z identyfikatorem eksportu "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" dla zasobu o nazwie "test" w grupie "test"</span><span class="sxs-lookup"><span data-stu-id="a607b-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a607b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a607b-113">PARAMETERS</span></span>

### <span data-ttu-id="a607b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a607b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a607b-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a607b-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a607b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a607b-116">-DefaultProfile</span></span>
<span data-ttu-id="a607b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a607b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a607b-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="a607b-118">-ExportId</span></span>
<span data-ttu-id="a607b-119">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a607b-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="a607b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a607b-120">-Name</span></span>
<span data-ttu-id="a607b-121">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a607b-121">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a607b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a607b-122">-PassThru</span></span>
<span data-ttu-id="a607b-123">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="a607b-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a607b-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a607b-124">This parameter is optional.</span></span> <span data-ttu-id="a607b-125">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="a607b-125">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a607b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a607b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a607b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a607b-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a607b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a607b-128">-ResourceId</span></span>
<span data-ttu-id="a607b-129">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a607b-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a607b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a607b-130">-Confirm</span></span>
<span data-ttu-id="a607b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a607b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a607b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a607b-132">-WhatIf</span></span>
<span data-ttu-id="a607b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a607b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a607b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a607b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a607b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a607b-135">CommonParameters</span></span>
<span data-ttu-id="a607b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a607b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a607b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a607b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a607b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a607b-138">INPUTS</span></span>

### <span data-ttu-id="a607b-139">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a607b-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="a607b-140">Parametry: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a607b-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="a607b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a607b-141">System.String</span></span>

## <span data-ttu-id="a607b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a607b-142">OUTPUTS</span></span>

### <span data-ttu-id="a607b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a607b-143">System.Boolean</span></span>

## <span data-ttu-id="a607b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a607b-144">NOTES</span></span>

## <span data-ttu-id="a607b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a607b-145">RELATED LINKS</span></span>

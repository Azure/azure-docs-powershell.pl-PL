---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: b2ada8c4a58b38eee9ab235bbcd88429934ac00c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956074"
---
# <span data-ttu-id="61bd8-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="61bd8-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="61bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="61bd8-103">Usuwanie konfiguracji ciągłego eksportu w zasobie szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="61bd8-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="61bd8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61bd8-104">SYNTAX</span></span>

### <span data-ttu-id="61bd8-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="61bd8-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61bd8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bd8-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61bd8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bd8-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bd8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="61bd8-108">DESCRIPTION</span></span>
<span data-ttu-id="61bd8-109">Usuwanie konfiguracji ciągłego eksportu w zasobie szczegółowych informacji o aplikacjach</span><span class="sxs-lookup"><span data-stu-id="61bd8-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="61bd8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61bd8-110">EXAMPLES</span></span>

### <span data-ttu-id="61bd8-111">Przykład 1. Usuwanie konfiguracji eksportu ciągłego w zasobie analizy aplikacji</span><span class="sxs-lookup"><span data-stu-id="61bd8-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="61bd8-112">Usuń konfigurację ciągłego eksportu aplikacji Insights z identyfikatorem eksportu "uGOoki0jQsyEs3IdQ83Q4QsNr4=" dla zasobu o nazwie "test" w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="61bd8-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="61bd8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61bd8-113">PARAMETERS</span></span>

### <span data-ttu-id="61bd8-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="61bd8-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="61bd8-115">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="61bd8-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="61bd8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bd8-116">-DefaultProfile</span></span>
<span data-ttu-id="61bd8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61bd8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61bd8-118">- ExportId</span><span class="sxs-lookup"><span data-stu-id="61bd8-118">-ExportId</span></span>
<span data-ttu-id="61bd8-119">Ciągły identyfikator eksportu aplikacji Insights.</span><span class="sxs-lookup"><span data-stu-id="61bd8-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="61bd8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="61bd8-120">-Name</span></span>
<span data-ttu-id="61bd8-121">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="61bd8-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="61bd8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61bd8-122">-PassThru</span></span>
<span data-ttu-id="61bd8-123">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="61bd8-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="61bd8-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="61bd8-124">This parameter is optional.</span></span> <span data-ttu-id="61bd8-125">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="61bd8-125">Default value is false.</span></span>

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

### <span data-ttu-id="61bd8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bd8-126">-ResourceGroupName</span></span>
<span data-ttu-id="61bd8-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61bd8-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="61bd8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61bd8-128">-ResourceId</span></span>
<span data-ttu-id="61bd8-129">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="61bd8-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="61bd8-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61bd8-130">-Confirm</span></span>
<span data-ttu-id="61bd8-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61bd8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bd8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bd8-132">-WhatIf</span></span>
<span data-ttu-id="61bd8-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61bd8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bd8-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="61bd8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bd8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bd8-135">CommonParameters</span></span>
<span data-ttu-id="61bd8-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61bd8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bd8-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bd8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bd8-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61bd8-138">INPUTS</span></span>

### <span data-ttu-id="61bd8-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="61bd8-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="61bd8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="61bd8-140">System.String</span></span>

## <span data-ttu-id="61bd8-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61bd8-141">OUTPUTS</span></span>

### <span data-ttu-id="61bd8-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61bd8-142">System.Boolean</span></span>

## <span data-ttu-id="61bd8-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61bd8-143">NOTES</span></span>

## <span data-ttu-id="61bd8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61bd8-144">RELATED LINKS</span></span>

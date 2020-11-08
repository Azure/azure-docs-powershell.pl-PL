---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234190"
---
# <span data-ttu-id="3da61-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="3da61-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="3da61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3da61-102">SYNOPSIS</span></span>
<span data-ttu-id="3da61-103">Usuwanie ciągłej konfiguracji eksportu w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="3da61-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="3da61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3da61-104">SYNTAX</span></span>

### <span data-ttu-id="3da61-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3da61-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3da61-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3da61-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3da61-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3da61-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3da61-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3da61-108">DESCRIPTION</span></span>
<span data-ttu-id="3da61-109">Usuwanie ciągłej konfiguracji eksportu w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="3da61-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="3da61-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3da61-110">EXAMPLES</span></span>

### <span data-ttu-id="3da61-111">Przykład 1 Usuwanie ciągłej konfiguracji eksportu w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="3da61-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="3da61-112">Usuwanie ciągłej konfiguracji eksportu w usłudze Application Insights z identyfikatorem eksportu "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" dla zasobu o nazwie "test" w grupie "test"</span><span class="sxs-lookup"><span data-stu-id="3da61-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="3da61-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3da61-113">PARAMETERS</span></span>

### <span data-ttu-id="3da61-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3da61-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3da61-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3da61-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="3da61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da61-116">-DefaultProfile</span></span>
<span data-ttu-id="3da61-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3da61-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da61-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="3da61-118">-ExportId</span></span>
<span data-ttu-id="3da61-119">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3da61-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="3da61-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3da61-120">-Name</span></span>
<span data-ttu-id="3da61-121">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3da61-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="3da61-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3da61-122">-PassThru</span></span>
<span data-ttu-id="3da61-123">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3da61-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="3da61-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3da61-124">This parameter is optional.</span></span> <span data-ttu-id="3da61-125">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="3da61-125">Default value is false.</span></span>

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

### <span data-ttu-id="3da61-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da61-126">-ResourceGroupName</span></span>
<span data-ttu-id="3da61-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3da61-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="3da61-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3da61-128">-ResourceId</span></span>
<span data-ttu-id="3da61-129">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3da61-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="3da61-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3da61-130">-Confirm</span></span>
<span data-ttu-id="3da61-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da61-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da61-132">-WhatIf</span></span>
<span data-ttu-id="3da61-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3da61-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3da61-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3da61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3da61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da61-135">CommonParameters</span></span>
<span data-ttu-id="3da61-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da61-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da61-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da61-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3da61-138">INPUTS</span></span>

### <span data-ttu-id="3da61-139">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3da61-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="3da61-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3da61-140">System.String</span></span>

## <span data-ttu-id="3da61-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3da61-141">OUTPUTS</span></span>

### <span data-ttu-id="3da61-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3da61-142">System.Boolean</span></span>

## <span data-ttu-id="3da61-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3da61-143">NOTES</span></span>

## <span data-ttu-id="3da61-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3da61-144">RELATED LINKS</span></span>

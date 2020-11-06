---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: ccccfe4ba17fe9d5fc9f35f6604f5f7bb9263d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550715"
---
# <span data-ttu-id="232c2-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="232c2-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="232c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="232c2-102">SYNOPSIS</span></span>
<span data-ttu-id="232c2-103">Usuwanie konfiguracji eksportu cotinuous w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="232c2-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="232c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="232c2-104">SYNTAX</span></span>

### <span data-ttu-id="232c2-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="232c2-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="232c2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="232c2-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232c2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="232c2-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="232c2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="232c2-108">DESCRIPTION</span></span>
<span data-ttu-id="232c2-109">Usuwanie konfiguracji eksportu cotinuous w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="232c2-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="232c2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="232c2-110">EXAMPLES</span></span>

### <span data-ttu-id="232c2-111">Przykład 1 Usuwanie konfiguracji eksportu cotinuous w zasobie Application Insights</span><span class="sxs-lookup"><span data-stu-id="232c2-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="232c2-112">Usuwanie ciągłej konfiguracji eksportu w usłudze Application Insights z identyfikatorem eksportu "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" dla zasobu o nazwie "test" w grupie "test"</span><span class="sxs-lookup"><span data-stu-id="232c2-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="232c2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="232c2-113">PARAMETERS</span></span>

### <span data-ttu-id="232c2-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="232c2-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="232c2-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="232c2-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="232c2-116">-Confirm</span></span>
<span data-ttu-id="232c2-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232c2-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232c2-118">-DefaultProfile</span></span>
<span data-ttu-id="232c2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="232c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="232c2-120">-ExportId</span></span>
<span data-ttu-id="232c2-121">Identyfikator eksportu w usłudze Application Insights.</span><span class="sxs-lookup"><span data-stu-id="232c2-121">Application Insights Continuous Export ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="232c2-122">-Name</span></span>
<span data-ttu-id="232c2-123">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="232c2-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="232c2-124">-PassThru</span></span>
<span data-ttu-id="232c2-125">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="232c2-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="232c2-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="232c2-126">This parameter is optional.</span></span> <span data-ttu-id="232c2-127">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="232c2-127">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="232c2-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="232c2-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="232c2-130">-ResourceId</span></span>
<span data-ttu-id="232c2-131">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="232c2-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232c2-132">-WhatIf</span></span>
<span data-ttu-id="232c2-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232c2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232c2-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="232c2-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232c2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232c2-135">CommonParameters</span></span>
<span data-ttu-id="232c2-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232c2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232c2-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="232c2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232c2-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="232c2-138">INPUTS</span></span>

### <span data-ttu-id="232c2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="232c2-139">System.String</span></span>

## <span data-ttu-id="232c2-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="232c2-140">OUTPUTS</span></span>

### <span data-ttu-id="232c2-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="232c2-141">System.Object</span></span>

## <span data-ttu-id="232c2-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="232c2-142">NOTES</span></span>

## <span data-ttu-id="232c2-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="232c2-143">RELATED LINKS</span></span>


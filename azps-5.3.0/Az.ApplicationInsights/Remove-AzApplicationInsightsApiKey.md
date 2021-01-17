---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381278"
---
# <span data-ttu-id="93b14-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="93b14-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="93b14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93b14-102">SYNOPSIS</span></span>
<span data-ttu-id="93b14-103">Usuwanie klucza API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="93b14-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="93b14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93b14-104">SYNTAX</span></span>

### <span data-ttu-id="93b14-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="93b14-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93b14-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93b14-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93b14-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93b14-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93b14-108">Opis</span><span class="sxs-lookup"><span data-stu-id="93b14-108">DESCRIPTION</span></span>
<span data-ttu-id="93b14-109">Usuwanie klucza API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="93b14-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="93b14-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93b14-110">EXAMPLES</span></span>

### <span data-ttu-id="93b14-111">Przykład 1 Usuwanie klucza interfejsu API usługi Application Insights dla zasobu usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="93b14-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="93b14-112">Usuń określony klucz interfejsu API usługi Application Insights o identyfikatorze "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" dla zasobu "test" w grupie zasobów "Tester".</span><span class="sxs-lookup"><span data-stu-id="93b14-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="93b14-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93b14-113">PARAMETERS</span></span>

### <span data-ttu-id="93b14-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="93b14-114">-ApiKeyId</span></span>
<span data-ttu-id="93b14-115">Identyfikator klucza API usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="93b14-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="93b14-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="93b14-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="93b14-117">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="93b14-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="93b14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b14-118">-DefaultProfile</span></span>
<span data-ttu-id="93b14-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93b14-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93b14-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93b14-120">-Name</span></span>
<span data-ttu-id="93b14-121">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="93b14-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="93b14-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93b14-122">-PassThru</span></span>
<span data-ttu-id="93b14-123">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="93b14-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="93b14-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="93b14-124">This parameter is optional.</span></span> <span data-ttu-id="93b14-125">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="93b14-125">Default value is false.</span></span>

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

### <span data-ttu-id="93b14-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b14-126">-ResourceGroupName</span></span>
<span data-ttu-id="93b14-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="93b14-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="93b14-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93b14-128">-ResourceId</span></span>
<span data-ttu-id="93b14-129">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="93b14-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="93b14-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93b14-130">-Confirm</span></span>
<span data-ttu-id="93b14-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93b14-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93b14-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93b14-132">-WhatIf</span></span>
<span data-ttu-id="93b14-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93b14-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93b14-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="93b14-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93b14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b14-135">CommonParameters</span></span>
<span data-ttu-id="93b14-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b14-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b14-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b14-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93b14-138">INPUTS</span></span>

### <span data-ttu-id="93b14-139">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="93b14-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="93b14-140">System. String</span><span class="sxs-lookup"><span data-stu-id="93b14-140">System.String</span></span>

## <span data-ttu-id="93b14-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93b14-141">OUTPUTS</span></span>

### <span data-ttu-id="93b14-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93b14-142">System.Boolean</span></span>

## <span data-ttu-id="93b14-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93b14-143">NOTES</span></span>

## <span data-ttu-id="93b14-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93b14-144">RELATED LINKS</span></span>

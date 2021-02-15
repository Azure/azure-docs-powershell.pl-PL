---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182250"
---
# <span data-ttu-id="1257b-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="1257b-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="1257b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1257b-102">SYNOPSIS</span></span>
<span data-ttu-id="1257b-103">Usuwanie klucza interfejsu API szczegółowych informacji aplikacji dla zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="1257b-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="1257b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1257b-104">SYNTAX</span></span>

### <span data-ttu-id="1257b-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1257b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1257b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1257b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1257b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1257b-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1257b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1257b-108">DESCRIPTION</span></span>
<span data-ttu-id="1257b-109">Usuwanie klucza interfejsu API szczegółowych informacji aplikacji dla zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="1257b-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="1257b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1257b-110">EXAMPLES</span></span>

### <span data-ttu-id="1257b-111">Przykład 1. Usunięcie klucza interfejsu API Insights aplikacji dla zasobu szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="1257b-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="1257b-112">Usuń określony klucz interfejsu API insights aplikacji, który ma identyfikator "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" dla zasobu "test" w grupie zasobów "testGroup".</span><span class="sxs-lookup"><span data-stu-id="1257b-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="1257b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1257b-113">PARAMETERS</span></span>

### <span data-ttu-id="1257b-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="1257b-114">-ApiKeyId</span></span>
<span data-ttu-id="1257b-115">Identyfikator klucza interfejsu API aplikacji Insights.</span><span class="sxs-lookup"><span data-stu-id="1257b-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="1257b-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1257b-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="1257b-117">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1257b-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="1257b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1257b-118">-DefaultProfile</span></span>
<span data-ttu-id="1257b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1257b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1257b-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1257b-120">-Name</span></span>
<span data-ttu-id="1257b-121">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1257b-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="1257b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1257b-122">-PassThru</span></span>
<span data-ttu-id="1257b-123">Jeśli zostanie określona, na wypadek, gdyby operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="1257b-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="1257b-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1257b-124">This parameter is optional.</span></span> <span data-ttu-id="1257b-125">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="1257b-125">Default value is false.</span></span>

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

### <span data-ttu-id="1257b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1257b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1257b-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1257b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="1257b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1257b-128">-ResourceId</span></span>
<span data-ttu-id="1257b-129">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1257b-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="1257b-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1257b-130">-Confirm</span></span>
<span data-ttu-id="1257b-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1257b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1257b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1257b-132">-WhatIf</span></span>
<span data-ttu-id="1257b-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1257b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1257b-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1257b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1257b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1257b-135">CommonParameters</span></span>
<span data-ttu-id="1257b-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1257b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1257b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1257b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1257b-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1257b-138">INPUTS</span></span>

### <span data-ttu-id="1257b-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1257b-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="1257b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1257b-140">System.String</span></span>

## <span data-ttu-id="1257b-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1257b-141">OUTPUTS</span></span>

### <span data-ttu-id="1257b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1257b-142">System.Boolean</span></span>

## <span data-ttu-id="1257b-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1257b-143">NOTES</span></span>

## <span data-ttu-id="1257b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1257b-144">RELATED LINKS</span></span>

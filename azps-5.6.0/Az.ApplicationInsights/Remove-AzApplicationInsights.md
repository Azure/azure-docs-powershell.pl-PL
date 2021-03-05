---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 089561268233876976598f3cf74cd0a52fef8402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004849"
---
# <span data-ttu-id="a37af-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a37af-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="a37af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a37af-102">SYNOPSIS</span></span>
<span data-ttu-id="a37af-103">Usuwanie zasobu szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="a37af-103">Remove an application insights resource</span></span>

## <span data-ttu-id="a37af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a37af-104">SYNTAX</span></span>

### <span data-ttu-id="a37af-105">ComponentNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a37af-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37af-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a37af-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37af-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a37af-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a37af-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a37af-108">DESCRIPTION</span></span>
<span data-ttu-id="a37af-109">Usuwanie zasobu szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="a37af-109">Remove an application insights resource</span></span>

## <span data-ttu-id="a37af-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a37af-110">EXAMPLES</span></span>

### <span data-ttu-id="a37af-111">Przykład 1. Usuwanie zasobu szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="a37af-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="a37af-112">Usuwanie zasobu szczegółowych informacji aplikacji o nazwie "test" w grupie zasobów "grupa testowa"</span><span class="sxs-lookup"><span data-stu-id="a37af-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a37af-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a37af-113">PARAMETERS</span></span>

### <span data-ttu-id="a37af-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a37af-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a37af-115">Obiekt składnika Szczegółowe informacje o aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a37af-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="a37af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37af-116">-DefaultProfile</span></span>
<span data-ttu-id="a37af-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a37af-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a37af-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a37af-118">-Name</span></span>
<span data-ttu-id="a37af-119">Nazwa składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a37af-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="a37af-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a37af-120">-PassThru</span></span>
<span data-ttu-id="a37af-121">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="a37af-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a37af-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a37af-122">This parameter is optional.</span></span> <span data-ttu-id="a37af-123">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="a37af-123">Default value is false.</span></span>

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

### <span data-ttu-id="a37af-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a37af-124">-ResourceGroupName</span></span>
<span data-ttu-id="a37af-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a37af-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a37af-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a37af-126">-ResourceId</span></span>
<span data-ttu-id="a37af-127">Identyfikator składnika szczegółowych informacji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a37af-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="a37af-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a37af-128">-Confirm</span></span>
<span data-ttu-id="a37af-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a37af-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a37af-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a37af-130">-WhatIf</span></span>
<span data-ttu-id="a37af-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a37af-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a37af-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a37af-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a37af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37af-133">CommonParameters</span></span>
<span data-ttu-id="a37af-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a37af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a37af-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a37af-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37af-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a37af-136">INPUTS</span></span>

### <span data-ttu-id="a37af-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a37af-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a37af-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a37af-138">System.String</span></span>

## <span data-ttu-id="a37af-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a37af-139">OUTPUTS</span></span>

### <span data-ttu-id="a37af-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a37af-140">System.Boolean</span></span>

## <span data-ttu-id="a37af-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a37af-141">NOTES</span></span>

## <span data-ttu-id="a37af-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a37af-142">RELATED LINKS</span></span>

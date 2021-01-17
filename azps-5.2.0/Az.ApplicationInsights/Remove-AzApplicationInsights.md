---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353485"
---
# <span data-ttu-id="9d442-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9d442-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="9d442-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d442-102">SYNOPSIS</span></span>
<span data-ttu-id="9d442-103">Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="9d442-103">Remove an application insights resource</span></span>

## <span data-ttu-id="9d442-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d442-104">SYNTAX</span></span>

### <span data-ttu-id="9d442-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d442-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d442-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d442-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d442-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d442-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d442-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9d442-108">DESCRIPTION</span></span>
<span data-ttu-id="9d442-109">Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="9d442-109">Remove an application insights resource</span></span>

## <span data-ttu-id="9d442-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d442-110">EXAMPLES</span></span>

### <span data-ttu-id="9d442-111">Przykład 1 Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="9d442-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="9d442-112">Usuwanie zasobu Usługa Application Insights o nazwie "test" w grupie zasobów "Grupa Tester"</span><span class="sxs-lookup"><span data-stu-id="9d442-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9d442-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d442-113">PARAMETERS</span></span>

### <span data-ttu-id="9d442-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9d442-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9d442-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9d442-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="9d442-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d442-116">-DefaultProfile</span></span>
<span data-ttu-id="9d442-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d442-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d442-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9d442-118">-Name</span></span>
<span data-ttu-id="9d442-119">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9d442-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="9d442-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d442-120">-PassThru</span></span>
<span data-ttu-id="9d442-121">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="9d442-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="9d442-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9d442-122">This parameter is optional.</span></span> <span data-ttu-id="9d442-123">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="9d442-123">Default value is false.</span></span>

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

### <span data-ttu-id="9d442-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d442-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d442-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9d442-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d442-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d442-126">-ResourceId</span></span>
<span data-ttu-id="9d442-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="9d442-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9d442-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d442-128">-Confirm</span></span>
<span data-ttu-id="9d442-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d442-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d442-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d442-130">-WhatIf</span></span>
<span data-ttu-id="9d442-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d442-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d442-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d442-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d442-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d442-133">CommonParameters</span></span>
<span data-ttu-id="9d442-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d442-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d442-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d442-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d442-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d442-136">INPUTS</span></span>

### <span data-ttu-id="9d442-137">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9d442-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="9d442-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9d442-138">System.String</span></span>

## <span data-ttu-id="9d442-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d442-139">OUTPUTS</span></span>

### <span data-ttu-id="9d442-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d442-140">System.Boolean</span></span>

## <span data-ttu-id="9d442-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d442-141">NOTES</span></span>

## <span data-ttu-id="9d442-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d442-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 5665b85a680411910513663d782791f56b7c1081
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706865"
---
# <span data-ttu-id="59784-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="59784-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="59784-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59784-102">SYNOPSIS</span></span>
<span data-ttu-id="59784-103">Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="59784-103">Remove an application insights resource</span></span>

## <span data-ttu-id="59784-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59784-104">SYNTAX</span></span>

### <span data-ttu-id="59784-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59784-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59784-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59784-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59784-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59784-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59784-108">Opis</span><span class="sxs-lookup"><span data-stu-id="59784-108">DESCRIPTION</span></span>
<span data-ttu-id="59784-109">Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="59784-109">Remove an application insights resource</span></span>

## <span data-ttu-id="59784-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59784-110">EXAMPLES</span></span>

### <span data-ttu-id="59784-111">Przykład 1 Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="59784-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="59784-112">Usuwanie zasobu Usługa Application Insights o nazwie "test" w grupie zasobów "Grupa Tester"</span><span class="sxs-lookup"><span data-stu-id="59784-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="59784-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59784-113">PARAMETERS</span></span>

### <span data-ttu-id="59784-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="59784-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="59784-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="59784-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="59784-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59784-116">-DefaultProfile</span></span>
<span data-ttu-id="59784-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59784-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59784-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59784-118">-Name</span></span>
<span data-ttu-id="59784-119">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="59784-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="59784-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59784-120">-PassThru</span></span>
<span data-ttu-id="59784-121">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="59784-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="59784-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="59784-122">This parameter is optional.</span></span> <span data-ttu-id="59784-123">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="59784-123">Default value is false.</span></span>

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

### <span data-ttu-id="59784-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59784-124">-ResourceGroupName</span></span>
<span data-ttu-id="59784-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59784-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="59784-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59784-126">-ResourceId</span></span>
<span data-ttu-id="59784-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="59784-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="59784-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59784-128">-Confirm</span></span>
<span data-ttu-id="59784-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59784-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59784-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59784-130">-WhatIf</span></span>
<span data-ttu-id="59784-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59784-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59784-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59784-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59784-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59784-133">CommonParameters</span></span>
<span data-ttu-id="59784-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59784-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59784-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59784-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59784-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59784-136">INPUTS</span></span>

### <span data-ttu-id="59784-137">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="59784-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="59784-138">System. String</span><span class="sxs-lookup"><span data-stu-id="59784-138">System.String</span></span>

## <span data-ttu-id="59784-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59784-139">OUTPUTS</span></span>

### <span data-ttu-id="59784-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59784-140">System.Boolean</span></span>

## <span data-ttu-id="59784-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59784-141">NOTES</span></span>

## <span data-ttu-id="59784-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59784-142">RELATED LINKS</span></span>
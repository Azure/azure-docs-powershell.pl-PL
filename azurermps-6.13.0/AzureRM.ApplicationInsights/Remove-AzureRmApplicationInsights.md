---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: 72a5affb91cbd2c1dfbe78cc7ee86da799b6ae50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524678"
---
# <span data-ttu-id="3622e-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3622e-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="3622e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3622e-102">SYNOPSIS</span></span>
<span data-ttu-id="3622e-103">Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="3622e-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3622e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3622e-104">SYNTAX</span></span>

### <span data-ttu-id="3622e-105">ComponentNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3622e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3622e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3622e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3622e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3622e-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3622e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3622e-108">DESCRIPTION</span></span>
<span data-ttu-id="3622e-109">Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="3622e-109">Remove an application insights resource</span></span>

## <span data-ttu-id="3622e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3622e-110">EXAMPLES</span></span>

### <span data-ttu-id="3622e-111">Przykład 1 Usuwanie zasobu Usługa Application Insights</span><span class="sxs-lookup"><span data-stu-id="3622e-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="3622e-112">Usuwanie zasobu applciation Insights o nazwie "test" w grupie zasób "</span><span class="sxs-lookup"><span data-stu-id="3622e-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="3622e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3622e-113">PARAMETERS</span></span>

### <span data-ttu-id="3622e-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3622e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3622e-115">Obiekt składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3622e-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="3622e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3622e-116">-DefaultProfile</span></span>
<span data-ttu-id="3622e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3622e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3622e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3622e-118">-Name</span></span>
<span data-ttu-id="3622e-119">Nazwa składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3622e-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="3622e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3622e-120">-PassThru</span></span>
<span data-ttu-id="3622e-121">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3622e-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="3622e-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3622e-122">This parameter is optional.</span></span> <span data-ttu-id="3622e-123">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="3622e-123">Default value is false.</span></span>

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

### <span data-ttu-id="3622e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3622e-124">-ResourceGroupName</span></span>
<span data-ttu-id="3622e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3622e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3622e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3622e-126">-ResourceId</span></span>
<span data-ttu-id="3622e-127">Identyfikator zasobu składnika Application Insights.</span><span class="sxs-lookup"><span data-stu-id="3622e-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="3622e-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3622e-128">-Confirm</span></span>
<span data-ttu-id="3622e-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3622e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3622e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3622e-130">-WhatIf</span></span>
<span data-ttu-id="3622e-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3622e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3622e-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3622e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3622e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3622e-133">CommonParameters</span></span>
<span data-ttu-id="3622e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3622e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3622e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3622e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3622e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3622e-136">INPUTS</span></span>

### <span data-ttu-id="3622e-137">Microsoft. Azure. Commands. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3622e-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="3622e-138">Parametry: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3622e-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="3622e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3622e-139">System.String</span></span>

## <span data-ttu-id="3622e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3622e-140">OUTPUTS</span></span>

### <span data-ttu-id="3622e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3622e-141">System.Boolean</span></span>

## <span data-ttu-id="3622e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3622e-142">NOTES</span></span>

## <span data-ttu-id="3622e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3622e-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: ed1550973882a8c012728c55899aec9a2f5d85f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980113"
---
# <span data-ttu-id="e92d6-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e92d6-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="e92d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e92d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e92d6-103">Pobiera reguły alertów.</span><span class="sxs-lookup"><span data-stu-id="e92d6-103">Gets alert rules.</span></span>

## <span data-ttu-id="e92d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e92d6-104">SYNTAX</span></span>

### <span data-ttu-id="e92d6-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e92d6-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e92d6-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="e92d6-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e92d6-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="e92d6-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e92d6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e92d6-108">DESCRIPTION</span></span>
<span data-ttu-id="e92d6-109">Polecenie **cmdlet Get-AzAlertRule** pobiera regułę alertu według jej nazwy, URI lub wszystkich reguł alertów z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e92d6-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="e92d6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e92d6-110">EXAMPLES</span></span>

### <span data-ttu-id="e92d6-111">Przykład 1. Uzyskiwanie reguł alertów dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e92d6-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="e92d6-112">To polecenie pobiera wszystkie reguły alertów dla grupy zasobów o nazwie Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="e92d6-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="e92d6-113">Dane wyjściowe nie zawierają szczegółowych informacji o zasadach, ponieważ nie *określono parametru DetailedOutput.*</span><span class="sxs-lookup"><span data-stu-id="e92d6-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="e92d6-114">Przykład 2. Uzyskiwanie reguły alertu według nazwy</span><span class="sxs-lookup"><span data-stu-id="e92d6-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="e92d6-115">To polecenie pobiera regułę alertu o nazwie myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="e92d6-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="e92d6-116">Ponieważ parametr *DetailedOutput* nie jest określony, dane wyjściowe zawierają tylko podstawowe informacje o regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="e92d6-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="e92d6-117">Przykład 3. Uzyskiwanie reguły alertu według nazwy ze szczegółowymi informacjami wyjściowym</span><span class="sxs-lookup"><span data-stu-id="e92d6-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="e92d6-118">To polecenie pobiera regułę alertu o nazwie myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="e92d6-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="e92d6-119">Parametr *DetailedOutput* jest określony, więc dane wyjściowe są szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="e92d6-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="e92d6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e92d6-120">PARAMETERS</span></span>

### <span data-ttu-id="e92d6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92d6-121">-DefaultProfile</span></span>
<span data-ttu-id="e92d6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e92d6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e92d6-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="e92d6-123">-DetailedOutput</span></span>
<span data-ttu-id="e92d6-124">Wyświetla pełne szczegóły w wyniku.</span><span class="sxs-lookup"><span data-stu-id="e92d6-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92d6-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e92d6-125">-Name</span></span>
<span data-ttu-id="e92d6-126">Określa nazwę reguły alertu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="e92d6-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="e92d6-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e92d6-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92d6-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e92d6-129">-TargetResourceId</span></span>
<span data-ttu-id="e92d6-130">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="e92d6-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92d6-131">CommonParameters</span></span>
<span data-ttu-id="e92d6-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e92d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92d6-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e92d6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92d6-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e92d6-134">INPUTS</span></span>

### <span data-ttu-id="e92d6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e92d6-135">System.String</span></span>

### <span data-ttu-id="e92d6-136">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e92d6-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e92d6-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e92d6-137">OUTPUTS</span></span>

### <span data-ttu-id="e92d6-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="e92d6-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="e92d6-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e92d6-139">NOTES</span></span>

## <span data-ttu-id="e92d6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e92d6-140">RELATED LINKS</span></span>

[<span data-ttu-id="e92d6-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e92d6-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="e92d6-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e92d6-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="e92d6-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e92d6-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="e92d6-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e92d6-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="e92d6-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e92d6-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)



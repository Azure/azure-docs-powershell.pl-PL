---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 9e1a0035a9736ac01963d150f06db9e510e51e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704825"
---
# <span data-ttu-id="66453-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="66453-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="66453-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66453-102">SYNOPSIS</span></span>
<span data-ttu-id="66453-103">Pobiera reguły alertów.</span><span class="sxs-lookup"><span data-stu-id="66453-103">Gets alert rules.</span></span>

## <span data-ttu-id="66453-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66453-104">SYNTAX</span></span>

### <span data-ttu-id="66453-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66453-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66453-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="66453-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66453-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="66453-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66453-108">Opis</span><span class="sxs-lookup"><span data-stu-id="66453-108">DESCRIPTION</span></span>
<span data-ttu-id="66453-109">Polecenie cmdlet **Get-AzAlertRule** pobiera regułę alertu przy użyciu jej nazwy lub identyfikatora URI lub wszystkich reguł alertów z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66453-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="66453-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66453-110">EXAMPLES</span></span>

### <span data-ttu-id="66453-111">Przykład 1: uzyskiwanie reguł alertów dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="66453-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="66453-112">To polecenie pobiera wszystkie reguły alertów dla grupy zasobów o nazwie Default-Web-Central.</span><span class="sxs-lookup"><span data-stu-id="66453-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="66453-113">Dane wyjściowe nie zawierają szczegółów dotyczących reguł, ponieważ nie określono parametru *DetailedOutput* .</span><span class="sxs-lookup"><span data-stu-id="66453-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="66453-114">Przykład 2: uzyskiwanie reguły alertu według nazwy</span><span class="sxs-lookup"><span data-stu-id="66453-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="66453-115">To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="66453-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="66453-116">Ponieważ parametr *DetailedOutput* nie jest określony, dane wyjściowe zawierają tylko podstawowe informacje na temat reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="66453-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="66453-117">Przykład 3: uzyskiwanie reguły alertu według nazwy z danymi szczegółowymi</span><span class="sxs-lookup"><span data-stu-id="66453-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="66453-118">To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="66453-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="66453-119">Określono parametr *DetailedOutput* , więc dane wyjściowe są szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="66453-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="66453-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66453-120">PARAMETERS</span></span>

### <span data-ttu-id="66453-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66453-121">-DefaultProfile</span></span>
<span data-ttu-id="66453-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="66453-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66453-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="66453-123">-DetailedOutput</span></span>
<span data-ttu-id="66453-124">Wyświetla wszystkie szczegóły w wynikach.</span><span class="sxs-lookup"><span data-stu-id="66453-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="66453-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66453-125">-Name</span></span>
<span data-ttu-id="66453-126">Określa nazwę reguły alertu, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="66453-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="66453-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66453-127">-ResourceGroupName</span></span>
<span data-ttu-id="66453-128">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66453-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="66453-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="66453-129">-TargetResourceId</span></span>
<span data-ttu-id="66453-130">Określa identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="66453-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="66453-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66453-131">CommonParameters</span></span>
<span data-ttu-id="66453-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66453-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66453-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66453-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66453-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66453-134">INPUTS</span></span>

### <span data-ttu-id="66453-135">System. String</span><span class="sxs-lookup"><span data-stu-id="66453-135">System.String</span></span>

### <span data-ttu-id="66453-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66453-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66453-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66453-137">OUTPUTS</span></span>

### <span data-ttu-id="66453-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="66453-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="66453-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66453-139">NOTES</span></span>

## <span data-ttu-id="66453-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66453-140">RELATED LINKS</span></span>

[<span data-ttu-id="66453-141">Dodaj-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="66453-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="66453-142">Dodaj-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="66453-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="66453-143">Dodaj-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="66453-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="66453-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="66453-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="66453-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="66453-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


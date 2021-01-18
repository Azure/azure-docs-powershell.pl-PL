---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503088"
---
# <span data-ttu-id="e2143-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e2143-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="e2143-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2143-102">SYNOPSIS</span></span>
<span data-ttu-id="e2143-103">Odrzuć zagregowany alert IoT</span><span class="sxs-lookup"><span data-stu-id="e2143-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="e2143-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2143-104">SYNTAX</span></span>

### <span data-ttu-id="e2143-105">SolutionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2143-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2143-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="e2143-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2143-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e2143-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2143-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e2143-108">DESCRIPTION</span></span>
<span data-ttu-id="e2143-109">Polecenie cmdlet Disable-AzIotSecurityAnalyticsAggregatedAlert odrzuca określony alert aggragated na urządzeniach Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="e2143-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="e2143-110">Nazwa zagregowanych alertów to kombinacja typu alertu i daty aggragted alertu rozdzielonej znakiem "/".</span><span class="sxs-lookup"><span data-stu-id="e2143-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="e2143-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2143-111">EXAMPLES</span></span>

### <span data-ttu-id="e2143-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2143-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="e2143-113">Odrzucanie zagregowanego alertu "IoT_SucessfulLocalLogin/2020-03-15" (nazwa połączona z typu alertu i jego zagregowaną datą) z rozwiązania zabezpieczeń IoT "Moja nazwa" w grupie zasób</span><span class="sxs-lookup"><span data-stu-id="e2143-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e2143-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e2143-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="e2143-115">Odrzuć zagregowany alert z identyfikatorem zasobu "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="e2143-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="e2143-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2143-116">PARAMETERS</span></span>

### <span data-ttu-id="e2143-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2143-117">-DefaultProfile</span></span>
<span data-ttu-id="e2143-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2143-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2143-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e2143-119">-InputObject</span></span>
<span data-ttu-id="e2143-120">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="e2143-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2143-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2143-121">-Name</span></span>
<span data-ttu-id="e2143-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e2143-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2143-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2143-123">-PassThru</span></span>
<span data-ttu-id="e2143-124">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e2143-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="e2143-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2143-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2143-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2143-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2143-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2143-127">-ResourceId</span></span>
<span data-ttu-id="e2143-128">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="e2143-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2143-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="e2143-129">-SolutionName</span></span>
<span data-ttu-id="e2143-130">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="e2143-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2143-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2143-131">-Confirm</span></span>
<span data-ttu-id="e2143-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2143-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2143-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2143-133">-WhatIf</span></span>
<span data-ttu-id="e2143-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2143-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2143-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2143-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2143-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2143-136">CommonParameters</span></span>
<span data-ttu-id="e2143-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2143-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2143-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2143-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2143-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2143-139">INPUTS</span></span>

### <span data-ttu-id="e2143-140">Microsoft. Azure. Commands. Security. models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e2143-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="e2143-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e2143-141">System.String</span></span>

## <span data-ttu-id="e2143-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2143-142">OUTPUTS</span></span>

### <span data-ttu-id="e2143-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2143-143">System.Boolean</span></span>

## <span data-ttu-id="e2143-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2143-144">NOTES</span></span>

## <span data-ttu-id="e2143-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2143-145">RELATED LINKS</span></span>

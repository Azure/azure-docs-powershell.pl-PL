---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340474"
---
# <span data-ttu-id="a19b9-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="a19b9-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="a19b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a19b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a19b9-103">Odrzuć zagregowany alert IoT</span><span class="sxs-lookup"><span data-stu-id="a19b9-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="a19b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a19b9-104">SYNTAX</span></span>

### <span data-ttu-id="a19b9-105">SolutionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a19b9-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a19b9-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a19b9-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a19b9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a19b9-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a19b9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a19b9-108">DESCRIPTION</span></span>
<span data-ttu-id="a19b9-109">Polecenie cmdlet Disable-AzIotSecurityAnalyticsAggregatedAlert odrzuca określony alert aggragated na urządzeniach Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="a19b9-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="a19b9-110">Nazwa zagregowanych alertów to kombinacja typu alertu i daty aggragted alertu rozdzielonej znakiem "/".</span><span class="sxs-lookup"><span data-stu-id="a19b9-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="a19b9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a19b9-111">EXAMPLES</span></span>

### <span data-ttu-id="a19b9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a19b9-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="a19b9-113">Odrzucanie zagregowanego alertu "IoT_SucessfulLocalLogin/2020-03-15" (nazwa połączona z typu alertu i jego zagregowaną datą) z rozwiązania zabezpieczeń IoT "Moja nazwa" w grupie zasób</span><span class="sxs-lookup"><span data-stu-id="a19b9-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="a19b9-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a19b9-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="a19b9-115">Odrzuć zagregowany alert z identyfikatorem zasobu "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="a19b9-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="a19b9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a19b9-116">PARAMETERS</span></span>

### <span data-ttu-id="a19b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19b9-117">-DefaultProfile</span></span>
<span data-ttu-id="a19b9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a19b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a19b9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a19b9-119">-InputObject</span></span>
<span data-ttu-id="a19b9-120">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="a19b9-120">Input Object.</span></span>

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

### <span data-ttu-id="a19b9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a19b9-121">-Name</span></span>
<span data-ttu-id="a19b9-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a19b9-122">Resource name.</span></span>

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

### <span data-ttu-id="a19b9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a19b9-123">-PassThru</span></span>
<span data-ttu-id="a19b9-124">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="a19b9-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a19b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="a19b9-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a19b9-126">Resource group name.</span></span>

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

### <span data-ttu-id="a19b9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a19b9-127">-ResourceId</span></span>
<span data-ttu-id="a19b9-128">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="a19b9-128">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a19b9-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="a19b9-129">-SolutionName</span></span>
<span data-ttu-id="a19b9-130">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="a19b9-130">Solution name</span></span>

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

### <span data-ttu-id="a19b9-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a19b9-131">-Confirm</span></span>
<span data-ttu-id="a19b9-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a19b9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a19b9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a19b9-133">-WhatIf</span></span>
<span data-ttu-id="a19b9-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a19b9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a19b9-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a19b9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a19b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19b9-136">CommonParameters</span></span>
<span data-ttu-id="a19b9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19b9-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a19b9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19b9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a19b9-139">INPUTS</span></span>

### <span data-ttu-id="a19b9-140">Microsoft. Azure. Commands. Security. models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="a19b9-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="a19b9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a19b9-141">System.String</span></span>

## <span data-ttu-id="a19b9-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a19b9-142">OUTPUTS</span></span>

### <span data-ttu-id="a19b9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a19b9-143">System.Boolean</span></span>

## <span data-ttu-id="a19b9-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a19b9-144">NOTES</span></span>

## <span data-ttu-id="a19b9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a19b9-145">RELATED LINKS</span></span>

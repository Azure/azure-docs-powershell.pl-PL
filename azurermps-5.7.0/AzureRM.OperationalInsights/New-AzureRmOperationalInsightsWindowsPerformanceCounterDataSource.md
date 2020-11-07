---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: b827c9d133ff6fc0bb9df0e1e3e25c3eea23916f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527989"
---
# <span data-ttu-id="28b81-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="28b81-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="28b81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28b81-102">SYNOPSIS</span></span>
<span data-ttu-id="28b81-103">Dodaje źródło danych liczników wydajności systemu Windows dla połączonych komputerów, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="28b81-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28b81-104">SYNTAX</span></span>

### <span data-ttu-id="28b81-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28b81-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b81-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="28b81-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28b81-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28b81-107">DESCRIPTION</span></span>
<span data-ttu-id="28b81-108">Polecenie cmdlet **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** umożliwia dodanie źródła danych liczników wydajności systemu Windows dla połączonych komputerów, na których jest uruchomiony system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="28b81-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="28b81-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28b81-109">EXAMPLES</span></span>

## <span data-ttu-id="28b81-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28b81-110">PARAMETERS</span></span>

### <span data-ttu-id="28b81-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="28b81-111">-CounterName</span></span>
<span data-ttu-id="28b81-112">Określa nazwę licznika.</span><span class="sxs-lookup"><span data-stu-id="28b81-112">Specifies the name of a counter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b81-113">-DefaultProfile</span></span>
<span data-ttu-id="28b81-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="28b81-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-115">-Force</span><span class="sxs-lookup"><span data-stu-id="28b81-115">-Force</span></span>
<span data-ttu-id="28b81-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28b81-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="28b81-117">-InstanceName</span></span>
<span data-ttu-id="28b81-118">Określa nazwę wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="28b81-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="28b81-119">-IntervalSeconds</span></span>
<span data-ttu-id="28b81-120">Określa interwał kolekcji.</span><span class="sxs-lookup"><span data-stu-id="28b81-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28b81-121">-Name</span></span>
<span data-ttu-id="28b81-122">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="28b81-122">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-123">-NazwaObiektu</span><span class="sxs-lookup"><span data-stu-id="28b81-123">-ObjectName</span></span>
<span data-ttu-id="28b81-124">Określa nazwę obiektu.</span><span class="sxs-lookup"><span data-stu-id="28b81-124">Specifies the name of an object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b81-125">-ResourceGroupName</span></span>
<span data-ttu-id="28b81-126">Określa nazwę grupy zasobów zawierającej komputery.</span><span class="sxs-lookup"><span data-stu-id="28b81-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="28b81-127">-UseLegacyCollector</span></span>
<span data-ttu-id="28b81-128">Użyj starszego modułu zbierającego lub domyślnego modułu zbierającego.</span><span class="sxs-lookup"><span data-stu-id="28b81-128">Use legacy collector or the default collector.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-129">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="28b81-129">-Workspace</span></span>
<span data-ttu-id="28b81-130">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b81-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="28b81-131">-WorkspaceName</span></span>
<span data-ttu-id="28b81-132">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b81-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28b81-133">-Confirm</span></span>
<span data-ttu-id="28b81-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b81-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b81-135">-WhatIf</span></span>
<span data-ttu-id="28b81-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b81-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b81-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28b81-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b81-138">CommonParameters</span></span>
<span data-ttu-id="28b81-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b81-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b81-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b81-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28b81-141">INPUTS</span></span>

### <span data-ttu-id="28b81-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="28b81-142">PSWorkspace</span></span>
<span data-ttu-id="28b81-143">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="28b81-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="28b81-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28b81-144">OUTPUTS</span></span>

### <span data-ttu-id="28b81-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="28b81-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="28b81-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28b81-146">NOTES</span></span>

## <span data-ttu-id="28b81-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28b81-147">RELATED LINKS</span></span>

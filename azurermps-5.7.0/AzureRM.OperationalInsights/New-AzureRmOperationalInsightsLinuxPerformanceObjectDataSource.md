---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: decae9e9282ad85832df676162f6bc684684f339
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719441"
---
# <span data-ttu-id="9f1f8-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="9f1f8-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="9f1f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1f8-103">Dodaje liczniki wydajności do wszystkich komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f1f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f1f8-104">SYNTAX</span></span>

### <span data-ttu-id="9f1f8-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9f1f8-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f1f8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9f1f8-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f1f8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9f1f8-107">DESCRIPTION</span></span>
<span data-ttu-id="9f1f8-108">Polecenie cmdlet **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** umożliwia dodanie liczników wydajności, z których usługa Azure Operational Insights gromadzi dane na wszystkich komputerach z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="9f1f8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f1f8-109">EXAMPLES</span></span>

## <span data-ttu-id="9f1f8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f1f8-110">PARAMETERS</span></span>

### <span data-ttu-id="9f1f8-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="9f1f8-111">-CounterNames</span></span>
<span data-ttu-id="9f1f8-112">Określa tablicę nazw liczników.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-112">Specifies an array of names of counters.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1f8-113">-DefaultProfile</span></span>
<span data-ttu-id="9f1f8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9f1f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f1f8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9f1f8-115">-Force</span></span>
<span data-ttu-id="9f1f8-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f1f8-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9f1f8-117">-InstanceName</span></span>
<span data-ttu-id="9f1f8-118">Określa nazwę wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="9f1f8-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="9f1f8-119">-IntervalSeconds</span></span>
<span data-ttu-id="9f1f8-120">Określa interwał kolekcji.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="9f1f8-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9f1f8-121">-Name</span></span>
<span data-ttu-id="9f1f8-122">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="9f1f8-123">-NazwaObiektu</span><span class="sxs-lookup"><span data-stu-id="9f1f8-123">-ObjectName</span></span>
<span data-ttu-id="9f1f8-124">Określa nazwę obiektu.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="9f1f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f1f8-126">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="9f1f8-127">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="9f1f8-127">-Workspace</span></span>
<span data-ttu-id="9f1f8-128">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9f1f8-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9f1f8-129">-WorkspaceName</span></span>
<span data-ttu-id="9f1f8-130">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9f1f8-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f1f8-131">-Confirm</span></span>
<span data-ttu-id="9f1f8-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f1f8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f1f8-133">-WhatIf</span></span>
<span data-ttu-id="9f1f8-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f1f8-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f1f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1f8-136">CommonParameters</span></span>
<span data-ttu-id="9f1f8-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1f8-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f1f8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1f8-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f1f8-139">INPUTS</span></span>

### <span data-ttu-id="9f1f8-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9f1f8-140">PSWorkspace</span></span>
<span data-ttu-id="9f1f8-141">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="9f1f8-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="9f1f8-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f1f8-142">OUTPUTS</span></span>

### <span data-ttu-id="9f1f8-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9f1f8-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9f1f8-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f1f8-144">NOTES</span></span>

## <span data-ttu-id="9f1f8-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f1f8-145">RELATED LINKS</span></span>

[<span data-ttu-id="9f1f8-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="9f1f8-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="9f1f8-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="9f1f8-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)



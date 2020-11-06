---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543128"
---
# <span data-ttu-id="e7bfa-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="e7bfa-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="e7bfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bfa-103">Dodaje liczniki wydajności do wszystkich komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7bfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7bfa-104">SYNTAX</span></span>

### <span data-ttu-id="e7bfa-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7bfa-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7bfa-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e7bfa-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7bfa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7bfa-107">DESCRIPTION</span></span>
<span data-ttu-id="e7bfa-108">Polecenie cmdlet **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** umożliwia dodanie liczników wydajności, z których usługa Azure Operational Insights gromadzi dane na wszystkich komputerach z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="e7bfa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7bfa-109">EXAMPLES</span></span>

## <span data-ttu-id="e7bfa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7bfa-110">PARAMETERS</span></span>

### <span data-ttu-id="e7bfa-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="e7bfa-111">-CounterNames</span></span>
<span data-ttu-id="e7bfa-112">Określa tablicę nazw liczników.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e7bfa-113">-Force</span></span>
<span data-ttu-id="e7bfa-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7bfa-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e7bfa-115">-InstanceName</span></span>
<span data-ttu-id="e7bfa-116">Określa nazwę wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-116">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="e7bfa-117">-IntervalSeconds</span></span>
<span data-ttu-id="e7bfa-118">Określa interwał kolekcji.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-118">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7bfa-119">-Name</span></span>
<span data-ttu-id="e7bfa-120">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-120">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-121">-NazwaObiektu</span><span class="sxs-lookup"><span data-stu-id="e7bfa-121">-ObjectName</span></span>
<span data-ttu-id="e7bfa-122">Określa nazwę obiektu.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-122">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7bfa-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7bfa-124">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-124">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-125">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="e7bfa-125">-Workspace</span></span>
<span data-ttu-id="e7bfa-126">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-126">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e7bfa-127">-WorkspaceName</span></span>
<span data-ttu-id="e7bfa-128">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7bfa-129">-Confirm</span></span>
<span data-ttu-id="e7bfa-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7bfa-131">-WhatIf</span></span>
<span data-ttu-id="e7bfa-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7bfa-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bfa-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7bfa-134">-DefaultProfile</span></span>
<span data-ttu-id="e7bfa-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7bfa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bfa-136">CommonParameters</span></span>
<span data-ttu-id="e7bfa-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7bfa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bfa-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7bfa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bfa-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7bfa-139">INPUTS</span></span>

### <span data-ttu-id="e7bfa-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e7bfa-140">PSWorkspace</span></span>
<span data-ttu-id="e7bfa-141">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="e7bfa-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e7bfa-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7bfa-142">OUTPUTS</span></span>

### <span data-ttu-id="e7bfa-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e7bfa-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e7bfa-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7bfa-144">NOTES</span></span>

## <span data-ttu-id="e7bfa-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7bfa-145">RELATED LINKS</span></span>

[<span data-ttu-id="e7bfa-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e7bfa-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e7bfa-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e7bfa-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)



---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 49d465b1d993542790c20833ff5b1f75e03d5f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554100"
---
# <span data-ttu-id="481bd-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="481bd-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="481bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="481bd-102">SYNOPSIS</span></span>
<span data-ttu-id="481bd-103">Dodaje źródło danych do komputerów z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="481bd-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="481bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="481bd-104">SYNTAX</span></span>

### <span data-ttu-id="481bd-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="481bd-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481bd-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="481bd-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="481bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="481bd-107">DESCRIPTION</span></span>
<span data-ttu-id="481bd-108">Polecenie cmdlet **New-AzureRmOperationalInsightsLinuxSyslogDataSource** umożliwia dodanie źródła danych dziennika systemowego do połączonych komputerów z systemem Linux w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="481bd-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="481bd-109">Usługa Azure Operational Insights może zbierać dane dziennika systemowego.</span><span class="sxs-lookup"><span data-stu-id="481bd-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="481bd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="481bd-110">EXAMPLES</span></span>

## <span data-ttu-id="481bd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="481bd-111">PARAMETERS</span></span>

### <span data-ttu-id="481bd-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="481bd-112">-CollectAlert</span></span>
<span data-ttu-id="481bd-113">Wskazuje, że komunikaty ostrzegawcze dotyczące obserwacji są zbierane.</span><span class="sxs-lookup"><span data-stu-id="481bd-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="481bd-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="481bd-114">-CollectCritical</span></span>
<span data-ttu-id="481bd-115">Wskazuje, że usługa Insights gromadzi wiadomości krytyczne.</span><span class="sxs-lookup"><span data-stu-id="481bd-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="481bd-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="481bd-116">-CollectDebug</span></span>
<span data-ttu-id="481bd-117">Wskazuje, że wiadomości debugowania w usłudze Insights są zbierane.</span><span class="sxs-lookup"><span data-stu-id="481bd-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="481bd-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="481bd-118">-CollectEmergency</span></span>
<span data-ttu-id="481bd-119">Wskazuje, że usługa Insights gromadzi wiadomości z awaryjnymi.</span><span class="sxs-lookup"><span data-stu-id="481bd-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="481bd-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="481bd-120">-CollectError</span></span>
<span data-ttu-id="481bd-121">Wskazuje, że usługa Insights gromadzi komunikaty o błędach.</span><span class="sxs-lookup"><span data-stu-id="481bd-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="481bd-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="481bd-122">-CollectInformational</span></span>
<span data-ttu-id="481bd-123">Wskazuje, że usługa Insights gromadzi wiadomości informacyjne.</span><span class="sxs-lookup"><span data-stu-id="481bd-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="481bd-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="481bd-124">-CollectNotice</span></span>
<span data-ttu-id="481bd-125">Wskazuje, że komunikaty o błędach działania są zbierane.</span><span class="sxs-lookup"><span data-stu-id="481bd-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="481bd-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="481bd-126">-CollectWarning</span></span>
<span data-ttu-id="481bd-127">Wskazuje, że dziennik systemowy zawiera komunikaty ostrzegawcze.</span><span class="sxs-lookup"><span data-stu-id="481bd-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="481bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481bd-128">-DefaultProfile</span></span>
<span data-ttu-id="481bd-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="481bd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="481bd-130">-Obiekt</span><span class="sxs-lookup"><span data-stu-id="481bd-130">-Facility</span></span>
<span data-ttu-id="481bd-131">Określa kod instrumentu.</span><span class="sxs-lookup"><span data-stu-id="481bd-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="481bd-132">-Force</span><span class="sxs-lookup"><span data-stu-id="481bd-132">-Force</span></span>
<span data-ttu-id="481bd-133">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="481bd-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="481bd-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="481bd-134">-Name</span></span>
<span data-ttu-id="481bd-135">Określa nazwę źródła danych.</span><span class="sxs-lookup"><span data-stu-id="481bd-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="481bd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="481bd-136">-ResourceGroupName</span></span>
<span data-ttu-id="481bd-137">Określa nazwę grupy zasobów zawierającej komputery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="481bd-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="481bd-138">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="481bd-138">-Workspace</span></span>
<span data-ttu-id="481bd-139">Określa obszar roboczy, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481bd-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="481bd-140">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="481bd-140">-WorkspaceName</span></span>
<span data-ttu-id="481bd-141">Określa nazwę obszaru roboczego, w którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481bd-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="481bd-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="481bd-142">-Confirm</span></span>
<span data-ttu-id="481bd-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481bd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="481bd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="481bd-144">-WhatIf</span></span>
<span data-ttu-id="481bd-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481bd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="481bd-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="481bd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="481bd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481bd-147">CommonParameters</span></span>
<span data-ttu-id="481bd-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="481bd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481bd-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="481bd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481bd-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="481bd-150">INPUTS</span></span>

### <span data-ttu-id="481bd-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="481bd-151">PSWorkspace</span></span>
<span data-ttu-id="481bd-152">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="481bd-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="481bd-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="481bd-153">OUTPUTS</span></span>

### <span data-ttu-id="481bd-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="481bd-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="481bd-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="481bd-155">NOTES</span></span>

## <span data-ttu-id="481bd-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="481bd-156">RELATED LINKS</span></span>

[<span data-ttu-id="481bd-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="481bd-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="481bd-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="481bd-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)



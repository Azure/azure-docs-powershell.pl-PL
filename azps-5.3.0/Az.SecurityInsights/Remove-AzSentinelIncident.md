---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502958"
---
# <span data-ttu-id="9915c-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9915c-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="9915c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9915c-102">SYNOPSIS</span></span>
<span data-ttu-id="9915c-103">Usuwanie incydentu.</span><span class="sxs-lookup"><span data-stu-id="9915c-103">Delete an Incident.</span></span>

## <span data-ttu-id="9915c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9915c-104">SYNTAX</span></span>

### <span data-ttu-id="9915c-105">IncidentId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9915c-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9915c-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9915c-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9915c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9915c-107">DESCRIPTION</span></span>
<span data-ttu-id="9915c-108">Polecenie cmdlet **Remove-AzSentinelIncident** powoduje trwałe usunięcie incydentu z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9915c-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="9915c-109">Obiekt **zdarzenia** można przekazać przy użyciu operatora potoku lub można też określić parametry wymagane.</span><span class="sxs-lookup"><span data-stu-id="9915c-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="9915c-110">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9915c-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9915c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9915c-111">EXAMPLES</span></span>

### <span data-ttu-id="9915c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9915c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="9915c-113">To polecenie usuwa zdarzenie z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9915c-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="9915c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9915c-114">PARAMETERS</span></span>

### <span data-ttu-id="9915c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9915c-115">-DefaultProfile</span></span>
<span data-ttu-id="9915c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9915c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9915c-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="9915c-117">-IncidentId</span></span>
<span data-ttu-id="9915c-118">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="9915c-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9915c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9915c-119">-InputObject</span></span>
<span data-ttu-id="9915c-120">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="9915c-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9915c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9915c-121">-PassThru</span></span>
<span data-ttu-id="9915c-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="9915c-122">PassThru</span></span>

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

### <span data-ttu-id="9915c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9915c-123">-ResourceGroupName</span></span>
<span data-ttu-id="9915c-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9915c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9915c-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9915c-125">-WorkspaceName</span></span>
<span data-ttu-id="9915c-126">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9915c-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9915c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9915c-127">-Confirm</span></span>
<span data-ttu-id="9915c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9915c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9915c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9915c-129">-WhatIf</span></span>
<span data-ttu-id="9915c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9915c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9915c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9915c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9915c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9915c-132">CommonParameters</span></span>
<span data-ttu-id="9915c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9915c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9915c-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9915c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9915c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9915c-135">INPUTS</span></span>

### <span data-ttu-id="9915c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9915c-136">System.String</span></span>
### <span data-ttu-id="9915c-137">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9915c-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="9915c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9915c-138">OUTPUTS</span></span>

### <span data-ttu-id="9915c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9915c-139">System.Boolean</span></span>
## <span data-ttu-id="9915c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9915c-140">NOTES</span></span>

## <span data-ttu-id="9915c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9915c-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502981"
---
# <span data-ttu-id="419b2-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="419b2-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="419b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="419b2-102">SYNOPSIS</span></span>
<span data-ttu-id="419b2-103">Zapoznaj się z incydentem.</span><span class="sxs-lookup"><span data-stu-id="419b2-103">Get an Incident.</span></span>

## <span data-ttu-id="419b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="419b2-104">SYNTAX</span></span>

### <span data-ttu-id="419b2-105">WorkspaceScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="419b2-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="419b2-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="419b2-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="419b2-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="419b2-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="419b2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="419b2-108">DESCRIPTION</span></span>
<span data-ttu-id="419b2-109">Polecenie cmdlet **Get-AzSentinelIncident** Pobiera zdarzenie z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="419b2-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="419b2-110">Jeśli określisz parametr *IncidentId* , zostanie zwrócony jeden obiekt **incydentu** .</span><span class="sxs-lookup"><span data-stu-id="419b2-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="419b2-111">Jeśli nie określisz parametru *IncidentId* , zostanie zwrócona tablica zawierająca wszystkie incydenty w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="419b2-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="419b2-112">W celu zaktualizowania incydentu można użyć obiektu **incydentu** , na przykład możesz dodać notatki do **incydentu**.</span><span class="sxs-lookup"><span data-stu-id="419b2-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="419b2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="419b2-113">EXAMPLES</span></span>

### <span data-ttu-id="419b2-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="419b2-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="419b2-115">W tym przykładzie są pobierane wszystkie **incydenty** w określonym obszarze roboczym, a następnie jest on przechowywany w zmiennej $incidents.</span><span class="sxs-lookup"><span data-stu-id="419b2-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="419b2-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="419b2-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="419b2-117">W tym przykładzie jest pobierana **incydent** w określonym obszarze roboczym, a następnie przechowywana w zmiennej $Incident.</span><span class="sxs-lookup"><span data-stu-id="419b2-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="419b2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="419b2-118">PARAMETERS</span></span>

### <span data-ttu-id="419b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="419b2-119">-DefaultProfile</span></span>
<span data-ttu-id="419b2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="419b2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="419b2-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="419b2-121">-IncidentId</span></span>
<span data-ttu-id="419b2-122">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="419b2-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="419b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="419b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="419b2-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="419b2-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419b2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="419b2-125">-ResourceId</span></span>
<span data-ttu-id="419b2-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="419b2-126">Resource Id.</span></span>

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

### <span data-ttu-id="419b2-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="419b2-127">-WorkspaceName</span></span>
<span data-ttu-id="419b2-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="419b2-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="419b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="419b2-129">CommonParameters</span></span>
<span data-ttu-id="419b2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="419b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="419b2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="419b2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="419b2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="419b2-132">INPUTS</span></span>

### <span data-ttu-id="419b2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="419b2-133">System.String</span></span>
## <span data-ttu-id="419b2-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="419b2-134">OUTPUTS</span></span>

### <span data-ttu-id="419b2-135">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="419b2-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="419b2-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="419b2-136">NOTES</span></span>

## <span data-ttu-id="419b2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="419b2-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: 669e0961327b6419e86f288ec71bffa6cdc69b4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986441"
---
# <span data-ttu-id="d54fa-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d54fa-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="d54fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d54fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d54fa-103">Uzyskaj zdarzenie.</span><span class="sxs-lookup"><span data-stu-id="d54fa-103">Get an Incident.</span></span>

## <span data-ttu-id="d54fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d54fa-104">SYNTAX</span></span>

### <span data-ttu-id="d54fa-105">WorkspaceScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d54fa-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d54fa-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="d54fa-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d54fa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d54fa-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d54fa-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d54fa-108">DESCRIPTION</span></span>
<span data-ttu-id="d54fa-109">Polecenie **cmdlet Get-AzSentinelIncident** pobiera polecenie Incident z określonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d54fa-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="d54fa-110">W przypadku określenia *parametru Identyfikator Zdarzenia* jest **zwracany** jeden obiekt Incident.</span><span class="sxs-lookup"><span data-stu-id="d54fa-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="d54fa-111">Jeśli parametr *IncidentId* nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie zdarzenia w określonym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="d54fa-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="d54fa-112">Za pomocą obiektu **Zdarzenie** można zaktualizować zdarzenie, na przykład możesz dodać notatki o **zdarzeniu.**</span><span class="sxs-lookup"><span data-stu-id="d54fa-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="d54fa-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d54fa-113">EXAMPLES</span></span>

### <span data-ttu-id="d54fa-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d54fa-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="d54fa-115">W tym przykładzie wszystkie zdarzenia **w** określonym obszarze roboczym są przechowywane w $Incidents danych.</span><span class="sxs-lookup"><span data-stu-id="d54fa-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="d54fa-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d54fa-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="d54fa-117">W tym przykładzie **zdarzenie jest przechowywane** w określonym obszarze roboczym, a następnie przechowywane w $Incident zmienną.</span><span class="sxs-lookup"><span data-stu-id="d54fa-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="d54fa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d54fa-118">PARAMETERS</span></span>

### <span data-ttu-id="d54fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d54fa-119">-DefaultProfile</span></span>
<span data-ttu-id="d54fa-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d54fa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d54fa-121">- IncidentId</span><span class="sxs-lookup"><span data-stu-id="d54fa-121">-IncidentId</span></span>
<span data-ttu-id="d54fa-122">Identyfikator zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="d54fa-122">Incident Id.</span></span>

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

### <span data-ttu-id="d54fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d54fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="d54fa-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d54fa-124">Resource group name.</span></span>

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

### <span data-ttu-id="d54fa-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d54fa-125">-ResourceId</span></span>
<span data-ttu-id="d54fa-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d54fa-126">Resource Id.</span></span>

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

### <span data-ttu-id="d54fa-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d54fa-127">-WorkspaceName</span></span>
<span data-ttu-id="d54fa-128">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="d54fa-128">Workspace Name.</span></span>

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

### <span data-ttu-id="d54fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d54fa-129">CommonParameters</span></span>
<span data-ttu-id="d54fa-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d54fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d54fa-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d54fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d54fa-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d54fa-132">INPUTS</span></span>

### <span data-ttu-id="d54fa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d54fa-133">System.String</span></span>
## <span data-ttu-id="d54fa-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d54fa-134">OUTPUTS</span></span>

### <span data-ttu-id="d54fa-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d54fa-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="d54fa-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d54fa-136">NOTES</span></span>

## <span data-ttu-id="d54fa-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d54fa-137">RELATED LINKS</span></span>

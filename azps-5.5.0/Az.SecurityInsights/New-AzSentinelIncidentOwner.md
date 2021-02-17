---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191211"
---
# <span data-ttu-id="64048-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="64048-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="64048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64048-102">SYNOPSIS</span></span>
<span data-ttu-id="64048-103">Tworzenie obiektu Właściciel zdarzenia w celu zaktualizowania właściciela zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="64048-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="64048-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64048-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64048-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="64048-105">DESCRIPTION</span></span>
<span data-ttu-id="64048-106">Polecenie **cmdlet New-AzSentinelIncidentOwner** tworzy w pamięci obiekt Właściciel zdarzenia w celu zaktualizowania zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="64048-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="64048-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64048-107">EXAMPLES</span></span>

### <span data-ttu-id="64048-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64048-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="64048-109">W tym przykładzie **jest tworzenie właściciela zdarzenia** i aktualizacja zdarzenia dla nowego właściciela.</span><span class="sxs-lookup"><span data-stu-id="64048-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="64048-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64048-110">PARAMETERS</span></span>

### <span data-ttu-id="64048-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="64048-111">-AssignedTo</span></span>
<span data-ttu-id="64048-112">Właściciel zdarzenia — Przypisano do</span><span class="sxs-lookup"><span data-stu-id="64048-112">Incident Owner - Assigned To</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64048-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64048-113">-DefaultProfile</span></span>
<span data-ttu-id="64048-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64048-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64048-115">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="64048-115">-Email</span></span>
<span data-ttu-id="64048-116">Właściciel zdarzenia — adres e-mail</span><span class="sxs-lookup"><span data-stu-id="64048-116">Incident Owner - Email</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64048-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="64048-117">-ObjectId</span></span>
<span data-ttu-id="64048-118">Właściciel zdarzenia — ObjectId</span><span class="sxs-lookup"><span data-stu-id="64048-118">Incident Owner - ObjectId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64048-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="64048-119">-UserPrincipalName</span></span>
<span data-ttu-id="64048-120">Właściciel zdarzenia — główna nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="64048-120">Incident Owner - User Principal Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64048-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64048-121">CommonParameters</span></span>
<span data-ttu-id="64048-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64048-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64048-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64048-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64048-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64048-124">INPUTS</span></span>

### <span data-ttu-id="64048-125">Brak</span><span class="sxs-lookup"><span data-stu-id="64048-125">None</span></span>
## <span data-ttu-id="64048-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64048-126">OUTPUTS</span></span>

### <span data-ttu-id="64048-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="64048-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="64048-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64048-128">NOTES</span></span>

## <span data-ttu-id="64048-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64048-129">RELATED LINKS</span></span>

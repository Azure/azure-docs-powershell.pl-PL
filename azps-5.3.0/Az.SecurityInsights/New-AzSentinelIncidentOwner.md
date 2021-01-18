---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502964"
---
# <span data-ttu-id="ec9f2-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="ec9f2-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="ec9f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9f2-103">Utwórz obiekt właściciel zdarzenia, aby zaktualizować właściciela zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="ec9f2-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="ec9f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec9f2-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec9f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec9f2-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9f2-106">Polecenie cmdlet **New-AzSentinelIncidentOwner** tworzy obiekt właściciel zdarzenia w pamięci w celu zaktualizowania incydentu.</span><span class="sxs-lookup"><span data-stu-id="ec9f2-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="ec9f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec9f2-107">EXAMPLES</span></span>

### <span data-ttu-id="ec9f2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec9f2-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="ec9f2-109">W tym przykładzie przedstawiono tworzenie **IncidentOwner** i aktualizowanie zdarzenia nowemu właścicielowi.</span><span class="sxs-lookup"><span data-stu-id="ec9f2-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="ec9f2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec9f2-110">PARAMETERS</span></span>

### <span data-ttu-id="ec9f2-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="ec9f2-111">-AssignedTo</span></span>
<span data-ttu-id="ec9f2-112">Właściciel incydentu przypisany do</span><span class="sxs-lookup"><span data-stu-id="ec9f2-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="ec9f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9f2-113">-DefaultProfile</span></span>
<span data-ttu-id="ec9f2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec9f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec9f2-115">-Mail</span><span class="sxs-lookup"><span data-stu-id="ec9f2-115">-Email</span></span>
<span data-ttu-id="ec9f2-116">Właściciel incydentu — adres E-mail</span><span class="sxs-lookup"><span data-stu-id="ec9f2-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="ec9f2-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec9f2-117">-ObjectId</span></span>
<span data-ttu-id="ec9f2-118">Właściciel zdarzenia-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec9f2-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="ec9f2-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ec9f2-119">-UserPrincipalName</span></span>
<span data-ttu-id="ec9f2-120">Właściciel zdarzenia — główna nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="ec9f2-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="ec9f2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9f2-121">CommonParameters</span></span>
<span data-ttu-id="ec9f2-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9f2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9f2-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec9f2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9f2-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec9f2-124">INPUTS</span></span>

### <span data-ttu-id="ec9f2-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ec9f2-125">None</span></span>
## <span data-ttu-id="ec9f2-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec9f2-126">OUTPUTS</span></span>

### <span data-ttu-id="ec9f2-127">Microsoft. Azure. Commands. SecurityInsights. modele. incydenty. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="ec9f2-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="ec9f2-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec9f2-128">NOTES</span></span>

## <span data-ttu-id="ec9f2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec9f2-129">RELATED LINKS</span></span>

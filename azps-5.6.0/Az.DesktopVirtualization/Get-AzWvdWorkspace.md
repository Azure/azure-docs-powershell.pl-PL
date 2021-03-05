---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 331026116b59e71d57b4ea440b53a1445ea7642b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980554"
---
# <span data-ttu-id="fc9f3-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="fc9f3-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="fc9f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9f3-103">Uzyskiwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-103">Get a workspace.</span></span>

## <span data-ttu-id="fc9f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc9f3-104">SYNTAX</span></span>

### <span data-ttu-id="fc9f3-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fc9f3-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fc9f3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fc9f3-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fc9f3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc9f3-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc9f3-108">Lista</span><span class="sxs-lookup"><span data-stu-id="fc9f3-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc9f3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc9f3-109">DESCRIPTION</span></span>
<span data-ttu-id="fc9f3-110">Uzyskiwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-110">Get a workspace.</span></span>

## <span data-ttu-id="fc9f3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc9f3-111">EXAMPLES</span></span>

### <span data-ttu-id="fc9f3-112">Przykład 1. Uzyskiwanie wirtualnego obszaru roboczego pulpitu systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="fc9f3-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="fc9f3-113">To polecenie otrzymuje obszar roboczy pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="fc9f3-114">Przykład 2. Lista obszarów roboczych pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="fc9f3-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="fc9f3-115">To polecenie wyświetla listę obszarów roboczych pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="fc9f3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc9f3-116">PARAMETERS</span></span>

### <span data-ttu-id="fc9f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc9f3-117">-DefaultProfile</span></span>
<span data-ttu-id="fc9f3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc9f3-119">-InputObject</span></span>
<span data-ttu-id="fc9f3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc9f3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fc9f3-121">-Name</span></span>
<span data-ttu-id="fc9f3-122">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="fc9f3-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc9f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc9f3-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-124">The name of the resource group.</span></span>
<span data-ttu-id="fc9f3-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9f3-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc9f3-126">-SubscriptionId</span></span>
<span data-ttu-id="fc9f3-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9f3-128">CommonParameters</span></span>
<span data-ttu-id="fc9f3-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9f3-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc9f3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9f3-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc9f3-131">INPUTS</span></span>

### <span data-ttu-id="fc9f3-132">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="fc9f3-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="fc9f3-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc9f3-133">OUTPUTS</span></span>

### <span data-ttu-id="fc9f3-134">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="fc9f3-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="fc9f3-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc9f3-135">NOTES</span></span>

<span data-ttu-id="fc9f3-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fc9f3-136">ALIASES</span></span>

<span data-ttu-id="fc9f3-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc9f3-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc9f3-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc9f3-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc9f3-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="fc9f3-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc9f3-141">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="fc9f3-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="fc9f3-142">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="fc9f3-143">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="fc9f3-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="fc9f3-144">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="fc9f3-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fc9f3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc9f3-146">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="fc9f3-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="fc9f3-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fc9f3-148">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="fc9f3-149">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="fc9f3-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="fc9f3-150">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fc9f3-151">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="fc9f3-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="fc9f3-152">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="fc9f3-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="fc9f3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc9f3-153">RELATED LINKS</span></span>


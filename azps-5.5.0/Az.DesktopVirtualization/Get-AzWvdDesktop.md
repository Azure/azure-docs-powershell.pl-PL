---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: de52995d5cda17e332c137966f58b349d64c01f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194523"
---
# <span data-ttu-id="e0ea1-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="e0ea1-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="e0ea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ea1-103">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-103">Get a desktop.</span></span>

## <span data-ttu-id="e0ea1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0ea1-104">SYNTAX</span></span>

### <span data-ttu-id="e0ea1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e0ea1-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0ea1-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e0ea1-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e0ea1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0ea1-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0ea1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0ea1-108">DESCRIPTION</span></span>
<span data-ttu-id="e0ea1-109">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-109">Get a desktop.</span></span>

## <span data-ttu-id="e0ea1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0ea1-110">EXAMPLES</span></span>

### <span data-ttu-id="e0ea1-111">Przykład 1. Uzyskiwanie pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="e0ea1-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="e0ea1-112">To polecenie pobiera pulpit wirtualny systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="e0ea1-113">Przykład 2. Lista pulpitów wirtualnych systemu Windows</span><span class="sxs-lookup"><span data-stu-id="e0ea1-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="e0ea1-114">To polecenie wyświetla listę pulpitów wirtualnych programuWindows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="e0ea1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0ea1-115">PARAMETERS</span></span>

### <span data-ttu-id="e0ea1-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ea1-116">-ApplicationGroupName</span></span>
<span data-ttu-id="e0ea1-117">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e0ea1-117">The name of the application group</span></span>

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

### <span data-ttu-id="e0ea1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ea1-118">-DefaultProfile</span></span>
<span data-ttu-id="e0ea1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ea1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0ea1-120">-InputObject</span></span>
<span data-ttu-id="e0ea1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0ea1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0ea1-122">-Name</span></span>
<span data-ttu-id="e0ea1-123">Nazwa pulpitu w określonej grupie pulpitu</span><span class="sxs-lookup"><span data-stu-id="e0ea1-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ea1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0ea1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-125">The name of the resource group.</span></span>
<span data-ttu-id="e0ea1-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e0ea1-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0ea1-127">-SubscriptionId</span></span>
<span data-ttu-id="e0ea1-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ea1-129">CommonParameters</span></span>
<span data-ttu-id="e0ea1-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ea1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0ea1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ea1-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ea1-132">INPUTS</span></span>

### <span data-ttu-id="e0ea1-133">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e0ea1-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e0ea1-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ea1-134">OUTPUTS</span></span>

### <span data-ttu-id="e0ea1-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="e0ea1-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="e0ea1-136">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="e0ea1-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="e0ea1-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0ea1-137">NOTES</span></span>

<span data-ttu-id="e0ea1-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e0ea1-138">ALIASES</span></span>

<span data-ttu-id="e0ea1-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0ea1-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0ea1-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0ea1-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0ea1-142">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e0ea1-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0ea1-143">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e0ea1-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e0ea1-144">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e0ea1-145">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="e0ea1-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e0ea1-146">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e0ea1-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e0ea1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0ea1-148">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="e0ea1-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="e0ea1-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e0ea1-150">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="e0ea1-151">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="e0ea1-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e0ea1-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e0ea1-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e0ea1-153">`[UserSessionId <String>]`: nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="e0ea1-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e0ea1-154">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="e0ea1-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e0ea1-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0ea1-155">RELATED LINKS</span></span>


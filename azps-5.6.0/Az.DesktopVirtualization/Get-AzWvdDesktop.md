---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 2c276ab6b791d041000adf872bf2bfb807032ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980586"
---
# <span data-ttu-id="21a15-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="21a15-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="21a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21a15-102">SYNOPSIS</span></span>
<span data-ttu-id="21a15-103">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="21a15-103">Get a desktop.</span></span>

## <span data-ttu-id="21a15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21a15-104">SYNTAX</span></span>

### <span data-ttu-id="21a15-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="21a15-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21a15-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="21a15-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21a15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="21a15-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="21a15-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="21a15-108">DESCRIPTION</span></span>
<span data-ttu-id="21a15-109">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="21a15-109">Get a desktop.</span></span>

## <span data-ttu-id="21a15-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21a15-110">EXAMPLES</span></span>

### <span data-ttu-id="21a15-111">Przykład 1. Uzyskiwanie pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="21a15-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="21a15-112">To polecenie pobiera pulpit wirtualny systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21a15-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="21a15-113">Przykład 2. Lista pulpitów wirtualnych systemu Windows</span><span class="sxs-lookup"><span data-stu-id="21a15-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="21a15-114">To polecenie wyświetla listę pulpitów wirtualnych programuWindows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21a15-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="21a15-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21a15-115">PARAMETERS</span></span>

### <span data-ttu-id="21a15-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="21a15-116">-ApplicationGroupName</span></span>
<span data-ttu-id="21a15-117">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="21a15-117">The name of the application group</span></span>

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

### <span data-ttu-id="21a15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a15-118">-DefaultProfile</span></span>
<span data-ttu-id="21a15-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21a15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a15-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a15-120">-InputObject</span></span>
<span data-ttu-id="21a15-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="21a15-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="21a15-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21a15-122">-Name</span></span>
<span data-ttu-id="21a15-123">Nazwa pulpitu w określonej grupie pulpitu</span><span class="sxs-lookup"><span data-stu-id="21a15-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="21a15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a15-124">-ResourceGroupName</span></span>
<span data-ttu-id="21a15-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21a15-125">The name of the resource group.</span></span>
<span data-ttu-id="21a15-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="21a15-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="21a15-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21a15-127">-SubscriptionId</span></span>
<span data-ttu-id="21a15-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="21a15-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="21a15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a15-129">CommonParameters</span></span>
<span data-ttu-id="21a15-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a15-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21a15-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a15-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21a15-132">INPUTS</span></span>

### <span data-ttu-id="21a15-133">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="21a15-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="21a15-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21a15-134">OUTPUTS</span></span>

### <span data-ttu-id="21a15-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="21a15-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="21a15-136">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="21a15-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="21a15-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21a15-137">NOTES</span></span>

<span data-ttu-id="21a15-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="21a15-138">ALIASES</span></span>

<span data-ttu-id="21a15-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21a15-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="21a15-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="21a15-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="21a15-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="21a15-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="21a15-142">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="21a15-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="21a15-143">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="21a15-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="21a15-144">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21a15-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="21a15-145">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="21a15-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="21a15-146">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21a15-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="21a15-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="21a15-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="21a15-148">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="21a15-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="21a15-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21a15-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="21a15-150">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="21a15-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="21a15-151">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="21a15-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="21a15-152">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="21a15-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="21a15-153">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="21a15-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="21a15-154">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="21a15-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="21a15-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21a15-155">RELATED LINKS</span></span>


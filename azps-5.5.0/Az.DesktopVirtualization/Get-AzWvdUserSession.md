---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 8dde4305003b97bd186a4601106a93e6f471edf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180770"
---
# <span data-ttu-id="22de7-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="22de7-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="22de7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22de7-102">SYNOPSIS</span></span>
<span data-ttu-id="22de7-103">Uzyskaj dostęp do userSession.</span><span class="sxs-lookup"><span data-stu-id="22de7-103">Get a userSession.</span></span>

## <span data-ttu-id="22de7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22de7-104">SYNTAX</span></span>

### <span data-ttu-id="22de7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="22de7-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="22de7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="22de7-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="22de7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="22de7-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="22de7-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="22de7-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="22de7-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="22de7-109">DESCRIPTION</span></span>
<span data-ttu-id="22de7-110">Uzyskaj userSession.</span><span class="sxs-lookup"><span data-stu-id="22de7-110">Get a userSession.</span></span>

## <span data-ttu-id="22de7-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22de7-111">EXAMPLES</span></span>

### <span data-ttu-id="22de7-112">Przykład 1. Uzyskiwanie sesji użytkowników pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="22de7-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="22de7-113">To polecenie otrzymuje polecenie UserSession pulpitu wirtualnego systemu Windows na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="22de7-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="22de7-114">Przykład 2. Lista użytkowników pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="22de7-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="22de7-115">To polecenie wyświetla listę użytkowników pulpitu wirtualnego systemu Windows na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="22de7-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="22de7-116">Przykład 3. Lista użytkowników pulpitu wirtualnego systemu Windows w puli hostów</span><span class="sxs-lookup"><span data-stu-id="22de7-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="22de7-117">To polecenie wyświetla listę użytkowników pulpitu wirtualnego systemu Windows na hoście sesji w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="22de7-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="22de7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22de7-118">PARAMETERS</span></span>

### <span data-ttu-id="22de7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22de7-119">-DefaultProfile</span></span>
<span data-ttu-id="22de7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22de7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22de7-121">— Filtr</span><span class="sxs-lookup"><span data-stu-id="22de7-121">-Filter</span></span>
<span data-ttu-id="22de7-122">Wyrażenie filtru OData.</span><span class="sxs-lookup"><span data-stu-id="22de7-122">OData filter expression.</span></span>
<span data-ttu-id="22de7-123">Prawidłowe właściwości filtrowania to userprincipalname (nazwa użytkownika) i sessionstate (Stan sesji).</span><span class="sxs-lookup"><span data-stu-id="22de7-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22de7-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="22de7-124">-HostPoolName</span></span>
<span data-ttu-id="22de7-125">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="22de7-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22de7-126">— Id</span><span class="sxs-lookup"><span data-stu-id="22de7-126">-Id</span></span>
<span data-ttu-id="22de7-127">Nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="22de7-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22de7-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22de7-128">-InputObject</span></span>
<span data-ttu-id="22de7-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="22de7-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="22de7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22de7-130">-ResourceGroupName</span></span>
<span data-ttu-id="22de7-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22de7-131">The name of the resource group.</span></span>
<span data-ttu-id="22de7-132">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="22de7-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22de7-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="22de7-133">-SessionHostName</span></span>
<span data-ttu-id="22de7-134">Nazwa hosta sesji w określonej puli hosta</span><span class="sxs-lookup"><span data-stu-id="22de7-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22de7-135">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22de7-135">-SubscriptionId</span></span>
<span data-ttu-id="22de7-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="22de7-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="22de7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22de7-137">CommonParameters</span></span>
<span data-ttu-id="22de7-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22de7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22de7-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22de7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22de7-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22de7-140">INPUTS</span></span>

### <span data-ttu-id="22de7-141">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="22de7-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="22de7-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22de7-142">OUTPUTS</span></span>

### <span data-ttu-id="22de7-143">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="22de7-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="22de7-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22de7-144">NOTES</span></span>

<span data-ttu-id="22de7-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="22de7-145">ALIASES</span></span>

<span data-ttu-id="22de7-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22de7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="22de7-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="22de7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="22de7-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="22de7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="22de7-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="22de7-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="22de7-150">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="22de7-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="22de7-151">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="22de7-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="22de7-152">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="22de7-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="22de7-153">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22de7-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="22de7-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="22de7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="22de7-155">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="22de7-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="22de7-156">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22de7-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="22de7-157">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="22de7-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="22de7-158">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="22de7-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="22de7-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="22de7-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="22de7-160">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="22de7-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="22de7-161">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="22de7-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="22de7-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22de7-162">RELATED LINKS</span></span>


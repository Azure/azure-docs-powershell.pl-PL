---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221227"
---
# <span data-ttu-id="91a33-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="91a33-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="91a33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91a33-102">SYNOPSIS</span></span>
<span data-ttu-id="91a33-103">Uzyskaj userSession.</span><span class="sxs-lookup"><span data-stu-id="91a33-103">Get a userSession.</span></span>

## <span data-ttu-id="91a33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91a33-104">SYNTAX</span></span>

### <span data-ttu-id="91a33-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="91a33-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91a33-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="91a33-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91a33-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91a33-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="91a33-108">List1</span><span class="sxs-lookup"><span data-stu-id="91a33-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="91a33-109">Opis</span><span class="sxs-lookup"><span data-stu-id="91a33-109">DESCRIPTION</span></span>
<span data-ttu-id="91a33-110">Uzyskaj userSession.</span><span class="sxs-lookup"><span data-stu-id="91a33-110">Get a userSession.</span></span>

## <span data-ttu-id="91a33-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91a33-111">EXAMPLES</span></span>

### <span data-ttu-id="91a33-112">Przykład 1: uzyskiwanie wirtualnego pulpitu systemu Windows UserSession według nazwy</span><span class="sxs-lookup"><span data-stu-id="91a33-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="91a33-113">To polecenie pobiera wirtualny pulpit systemu Windows UserSession na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="91a33-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="91a33-114">Przykład 2: Wyświetlanie listy pulpitów wirtualnych systemu UserSessions</span><span class="sxs-lookup"><span data-stu-id="91a33-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="91a33-115">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu UserSessions na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="91a33-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="91a33-116">Przykład 3: Wyświetlanie listy pulpitów wirtualnych systemu UserSessions w puli hostów</span><span class="sxs-lookup"><span data-stu-id="91a33-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="91a33-117">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu UserSessions na hoście sesji w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="91a33-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="91a33-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91a33-118">PARAMETERS</span></span>

### <span data-ttu-id="91a33-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a33-119">-DefaultProfile</span></span>
<span data-ttu-id="91a33-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91a33-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91a33-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="91a33-121">-Filter</span></span>
<span data-ttu-id="91a33-122">Wyrażenie filtru OData.</span><span class="sxs-lookup"><span data-stu-id="91a33-122">OData filter expression.</span></span>
<span data-ttu-id="91a33-123">Prawidłowe właściwości filtrowania to userPrincipalName i sessionState.</span><span class="sxs-lookup"><span data-stu-id="91a33-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="91a33-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="91a33-124">-HostPoolName</span></span>
<span data-ttu-id="91a33-125">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="91a33-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="91a33-126">-ID</span><span class="sxs-lookup"><span data-stu-id="91a33-126">-Id</span></span>
<span data-ttu-id="91a33-127">Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="91a33-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="91a33-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91a33-128">-InputObject</span></span>
<span data-ttu-id="91a33-129">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="91a33-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91a33-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a33-130">-ResourceGroupName</span></span>
<span data-ttu-id="91a33-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91a33-131">The name of the resource group.</span></span>
<span data-ttu-id="91a33-132">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="91a33-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="91a33-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="91a33-133">-SessionHostName</span></span>
<span data-ttu-id="91a33-134">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="91a33-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="91a33-135">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="91a33-135">-SubscriptionId</span></span>
<span data-ttu-id="91a33-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="91a33-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="91a33-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a33-137">CommonParameters</span></span>
<span data-ttu-id="91a33-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a33-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a33-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91a33-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a33-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91a33-140">INPUTS</span></span>

### <span data-ttu-id="91a33-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="91a33-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="91a33-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91a33-142">OUTPUTS</span></span>

### <span data-ttu-id="91a33-143">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="91a33-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="91a33-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91a33-144">NOTES</span></span>

<span data-ttu-id="91a33-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="91a33-145">ALIASES</span></span>

<span data-ttu-id="91a33-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91a33-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91a33-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="91a33-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91a33-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91a33-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91a33-149">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="91a33-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91a33-150">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="91a33-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="91a33-151">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="91a33-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="91a33-152">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="91a33-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="91a33-153">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="91a33-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="91a33-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="91a33-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91a33-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91a33-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="91a33-156">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="91a33-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="91a33-157">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="91a33-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="91a33-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="91a33-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="91a33-159">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="91a33-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="91a33-160">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="91a33-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="91a33-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91a33-161">RELATED LINKS</span></span>


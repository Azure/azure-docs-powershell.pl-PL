---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 0b0a044b9521236c3a29e7deffa15840b6d039ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369462"
---
# <span data-ttu-id="c8943-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="c8943-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="c8943-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8943-102">SYNOPSIS</span></span>
<span data-ttu-id="c8943-103">Uzyskaj userSession.</span><span class="sxs-lookup"><span data-stu-id="c8943-103">Get a userSession.</span></span>

## <span data-ttu-id="c8943-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8943-104">SYNTAX</span></span>

### <span data-ttu-id="c8943-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c8943-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8943-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c8943-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8943-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8943-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8943-108">List1</span><span class="sxs-lookup"><span data-stu-id="c8943-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c8943-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c8943-109">DESCRIPTION</span></span>
<span data-ttu-id="c8943-110">Uzyskaj userSession.</span><span class="sxs-lookup"><span data-stu-id="c8943-110">Get a userSession.</span></span>

## <span data-ttu-id="c8943-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8943-111">EXAMPLES</span></span>

### <span data-ttu-id="c8943-112">Przykład 1: uzyskiwanie wirtualnego pulpitu systemu Windows UserSession według nazwy</span><span class="sxs-lookup"><span data-stu-id="c8943-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="c8943-113">To polecenie pobiera wirtualny pulpit systemu Windows UserSession na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="c8943-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="c8943-114">Przykład 2: Wyświetlanie listy pulpitów wirtualnych systemu UserSessions</span><span class="sxs-lookup"><span data-stu-id="c8943-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="c8943-115">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu UserSessions na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="c8943-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="c8943-116">Przykład 3: Wyświetlanie listy pulpitów wirtualnych systemu UserSessions w puli hostów</span><span class="sxs-lookup"><span data-stu-id="c8943-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="c8943-117">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu UserSessions na hoście sesji w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="c8943-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="c8943-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8943-118">PARAMETERS</span></span>

### <span data-ttu-id="c8943-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8943-119">-DefaultProfile</span></span>
<span data-ttu-id="c8943-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8943-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8943-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="c8943-121">-Filter</span></span>
<span data-ttu-id="c8943-122">Wyrażenie filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c8943-122">OData filter expression.</span></span>
<span data-ttu-id="c8943-123">Prawidłowe właściwości filtrowania to userPrincipalName i sessionState.</span><span class="sxs-lookup"><span data-stu-id="c8943-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="c8943-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c8943-124">-HostPoolName</span></span>
<span data-ttu-id="c8943-125">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c8943-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="c8943-126">-ID</span><span class="sxs-lookup"><span data-stu-id="c8943-126">-Id</span></span>
<span data-ttu-id="c8943-127">Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="c8943-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="c8943-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8943-128">-InputObject</span></span>
<span data-ttu-id="c8943-129">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c8943-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8943-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8943-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8943-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8943-131">The name of the resource group.</span></span>
<span data-ttu-id="c8943-132">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c8943-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c8943-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="c8943-133">-SessionHostName</span></span>
<span data-ttu-id="c8943-134">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="c8943-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="c8943-135">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c8943-135">-SubscriptionId</span></span>
<span data-ttu-id="c8943-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c8943-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c8943-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8943-137">CommonParameters</span></span>
<span data-ttu-id="c8943-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8943-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8943-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8943-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8943-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8943-140">INPUTS</span></span>

### <span data-ttu-id="c8943-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c8943-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c8943-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8943-142">OUTPUTS</span></span>

### <span data-ttu-id="c8943-143">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="c8943-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IUserSession</span></span>

## <span data-ttu-id="c8943-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8943-144">NOTES</span></span>

<span data-ttu-id="c8943-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c8943-145">ALIASES</span></span>

<span data-ttu-id="c8943-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8943-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8943-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c8943-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8943-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8943-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8943-149">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c8943-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8943-150">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c8943-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c8943-151">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="c8943-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c8943-152">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="c8943-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c8943-153">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c8943-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c8943-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c8943-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8943-155">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="c8943-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c8943-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8943-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c8943-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c8943-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="c8943-158">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="c8943-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c8943-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c8943-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c8943-160">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="c8943-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c8943-161">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="c8943-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c8943-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8943-162">RELATED LINKS</span></span>


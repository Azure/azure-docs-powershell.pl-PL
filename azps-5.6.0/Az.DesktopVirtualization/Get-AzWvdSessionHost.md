---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 1e7727933f01f1b2fa3196e3c195c25dda5c247b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962017"
---
# <span data-ttu-id="9819b-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="9819b-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="9819b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9819b-102">SYNOPSIS</span></span>
<span data-ttu-id="9819b-103">Uzyskaj hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="9819b-103">Get a session host.</span></span>

## <span data-ttu-id="9819b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9819b-104">SYNTAX</span></span>

### <span data-ttu-id="9819b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9819b-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9819b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="9819b-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9819b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9819b-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9819b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9819b-108">DESCRIPTION</span></span>
<span data-ttu-id="9819b-109">Uzyskaj hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="9819b-109">Get a session host.</span></span>

## <span data-ttu-id="9819b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9819b-110">EXAMPLES</span></span>

### <span data-ttu-id="9819b-111">Przykład 1. Uzyskiwanie hosta SessionHost pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="9819b-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="9819b-112">To polecenie otrzymuje hosta SessionHost pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="9819b-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="9819b-113">Przykład 2. Lista hostów sesji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="9819b-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="9819b-114">To polecenie wyświetla listę hostów sesji pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="9819b-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="9819b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9819b-115">PARAMETERS</span></span>

### <span data-ttu-id="9819b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9819b-116">-DefaultProfile</span></span>
<span data-ttu-id="9819b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9819b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9819b-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="9819b-118">-HostPoolName</span></span>
<span data-ttu-id="9819b-119">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="9819b-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="9819b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9819b-120">-InputObject</span></span>
<span data-ttu-id="9819b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9819b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9819b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9819b-122">-Name</span></span>
<span data-ttu-id="9819b-123">Nazwa hosta sesji w określonej puli hosta</span><span class="sxs-lookup"><span data-stu-id="9819b-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9819b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9819b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9819b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9819b-125">The name of the resource group.</span></span>
<span data-ttu-id="9819b-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9819b-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9819b-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9819b-127">-SubscriptionId</span></span>
<span data-ttu-id="9819b-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9819b-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9819b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9819b-129">CommonParameters</span></span>
<span data-ttu-id="9819b-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9819b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9819b-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9819b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9819b-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9819b-132">INPUTS</span></span>

### <span data-ttu-id="9819b-133">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="9819b-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="9819b-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9819b-134">OUTPUTS</span></span>

### <span data-ttu-id="9819b-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="9819b-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="9819b-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9819b-136">NOTES</span></span>

<span data-ttu-id="9819b-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9819b-137">ALIASES</span></span>

<span data-ttu-id="9819b-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9819b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9819b-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9819b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9819b-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9819b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9819b-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9819b-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9819b-142">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="9819b-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="9819b-143">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9819b-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="9819b-144">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="9819b-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="9819b-145">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9819b-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="9819b-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9819b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9819b-147">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="9819b-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="9819b-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9819b-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9819b-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="9819b-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="9819b-150">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="9819b-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="9819b-151">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="9819b-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9819b-152">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="9819b-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="9819b-153">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="9819b-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="9819b-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9819b-154">RELATED LINKS</span></span>


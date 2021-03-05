---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: b7aa21b07726140f8f6514fe8d7b6dc9a4b191dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962058"
---
# <span data-ttu-id="c5340-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="c5340-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="c5340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5340-102">SYNOPSIS</span></span>
<span data-ttu-id="c5340-103">Pobierz aplikację.</span><span class="sxs-lookup"><span data-stu-id="c5340-103">Get an application.</span></span>

## <span data-ttu-id="c5340-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c5340-104">SYNTAX</span></span>

### <span data-ttu-id="c5340-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c5340-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5340-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c5340-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5340-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c5340-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5340-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c5340-108">DESCRIPTION</span></span>
<span data-ttu-id="c5340-109">Pobierz aplikację.</span><span class="sxs-lookup"><span data-stu-id="c5340-109">Get an application.</span></span>

## <span data-ttu-id="c5340-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c5340-110">EXAMPLES</span></span>

### <span data-ttu-id="c5340-111">Przykład 1. Uzyskiwanie aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="c5340-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="c5340-112">To polecenie otrzymuje aplikację pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5340-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="c5340-113">Przykład 2. Lista aplikacji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="c5340-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="c5340-114">To polecenie wyświetla listę aplikacji pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5340-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="c5340-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5340-115">PARAMETERS</span></span>

### <span data-ttu-id="c5340-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5340-116">-DefaultProfile</span></span>
<span data-ttu-id="c5340-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5340-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5340-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="c5340-118">-GroupName</span></span>
<span data-ttu-id="c5340-119">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5340-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5340-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5340-120">-InputObject</span></span>
<span data-ttu-id="c5340-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c5340-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c5340-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c5340-122">-Name</span></span>
<span data-ttu-id="c5340-123">Nazwa aplikacji w obrębie określonej grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5340-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5340-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5340-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5340-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5340-125">The name of the resource group.</span></span>
<span data-ttu-id="c5340-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c5340-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c5340-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5340-127">-SubscriptionId</span></span>
<span data-ttu-id="c5340-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c5340-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c5340-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5340-129">CommonParameters</span></span>
<span data-ttu-id="c5340-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5340-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5340-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5340-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5340-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5340-132">INPUTS</span></span>

### <span data-ttu-id="c5340-133">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c5340-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c5340-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5340-134">OUTPUTS</span></span>

### <span data-ttu-id="c5340-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="c5340-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="c5340-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c5340-136">NOTES</span></span>

<span data-ttu-id="c5340-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c5340-137">ALIASES</span></span>

<span data-ttu-id="c5340-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5340-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5340-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c5340-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5340-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c5340-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5340-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="c5340-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c5340-142">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5340-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c5340-143">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5340-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c5340-144">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="c5340-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c5340-145">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5340-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c5340-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c5340-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c5340-147">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="c5340-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c5340-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5340-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c5340-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="c5340-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="c5340-150">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="c5340-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c5340-151">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c5340-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c5340-152">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="c5340-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c5340-153">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="c5340-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c5340-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5340-154">RELATED LINKS</span></span>


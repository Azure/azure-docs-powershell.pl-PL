---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 480c1d5517aa79ff7b3a0fa5dfa24f2ae6f4ae45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200515"
---
# <span data-ttu-id="3c652-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="3c652-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="3c652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c652-102">SYNOPSIS</span></span>
<span data-ttu-id="3c652-103">Uzyskaj pulę hosta.</span><span class="sxs-lookup"><span data-stu-id="3c652-103">Get a host pool.</span></span>

## <span data-ttu-id="3c652-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c652-104">SYNTAX</span></span>

### <span data-ttu-id="3c652-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3c652-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3c652-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3c652-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3c652-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c652-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c652-108">Lista</span><span class="sxs-lookup"><span data-stu-id="3c652-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c652-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c652-109">DESCRIPTION</span></span>
<span data-ttu-id="3c652-110">Uzyskaj pulę hosta.</span><span class="sxs-lookup"><span data-stu-id="3c652-110">Get a host pool.</span></span>

## <span data-ttu-id="3c652-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c652-111">EXAMPLES</span></span>

### <span data-ttu-id="3c652-112">Przykład 1. Uzyskiwanie buforu hosta pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="3c652-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="3c652-113">To polecenie pobiera do grupy zasobów bufor pulpitu wirtualnego systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="3c652-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="3c652-114">Przykład 2. Lista buforów hostów pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="3c652-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="3c652-115">To polecenie wyświetla listę buforów hostów pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c652-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="3c652-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c652-116">PARAMETERS</span></span>

### <span data-ttu-id="3c652-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c652-117">-DefaultProfile</span></span>
<span data-ttu-id="3c652-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c652-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c652-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c652-119">-InputObject</span></span>
<span data-ttu-id="3c652-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3c652-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c652-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3c652-121">-Name</span></span>
<span data-ttu-id="3c652-122">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="3c652-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c652-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c652-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c652-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c652-124">The name of the resource group.</span></span>
<span data-ttu-id="3c652-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3c652-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3c652-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c652-126">-SubscriptionId</span></span>
<span data-ttu-id="3c652-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3c652-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3c652-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c652-128">CommonParameters</span></span>
<span data-ttu-id="3c652-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c652-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c652-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c652-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c652-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c652-131">INPUTS</span></span>

### <span data-ttu-id="3c652-132">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3c652-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3c652-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c652-133">OUTPUTS</span></span>

### <span data-ttu-id="3c652-134">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="3c652-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="3c652-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c652-135">NOTES</span></span>

<span data-ttu-id="3c652-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3c652-136">ALIASES</span></span>

<span data-ttu-id="3c652-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="3c652-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c652-138">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3c652-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c652-139">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c652-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c652-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3c652-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c652-141">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3c652-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3c652-142">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3c652-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3c652-143">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="3c652-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3c652-144">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c652-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3c652-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3c652-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c652-146">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="3c652-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3c652-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c652-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3c652-148">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3c652-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="3c652-149">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="3c652-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3c652-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3c652-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3c652-151">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="3c652-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3c652-152">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="3c652-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3c652-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c652-153">RELATED LINKS</span></span>


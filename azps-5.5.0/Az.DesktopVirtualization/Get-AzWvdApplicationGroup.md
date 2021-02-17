---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180818"
---
# <span data-ttu-id="11bb5-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="11bb5-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="11bb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="11bb5-103">Pobierz grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="11bb5-103">Get an application group.</span></span>

## <span data-ttu-id="11bb5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11bb5-104">SYNTAX</span></span>

### <span data-ttu-id="11bb5-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="11bb5-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="11bb5-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="11bb5-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11bb5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11bb5-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="11bb5-108">Lista</span><span class="sxs-lookup"><span data-stu-id="11bb5-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="11bb5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="11bb5-109">DESCRIPTION</span></span>
<span data-ttu-id="11bb5-110">Pobierz grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="11bb5-110">Get an application group.</span></span>

## <span data-ttu-id="11bb5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11bb5-111">EXAMPLES</span></span>

### <span data-ttu-id="11bb5-112">Przykład 1. Uzyskiwanie grupy aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="11bb5-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="11bb5-113">To polecenie pobiera grupę aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="11bb5-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="11bb5-114">Przykład 2. Lista grup aplikacji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="11bb5-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="11bb5-115">To polecenie wyświetla listę grup aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="11bb5-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="11bb5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11bb5-116">PARAMETERS</span></span>

### <span data-ttu-id="11bb5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bb5-117">-DefaultProfile</span></span>
<span data-ttu-id="11bb5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11bb5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11bb5-119">— Filtr</span><span class="sxs-lookup"><span data-stu-id="11bb5-119">-Filter</span></span>
<span data-ttu-id="11bb5-120">Wyrażenie filtru OData.</span><span class="sxs-lookup"><span data-stu-id="11bb5-120">OData filter expression.</span></span>
<span data-ttu-id="11bb5-121">Prawidłowe właściwości filtrowania to applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="11bb5-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11bb5-122">-InputObject</span></span>
<span data-ttu-id="11bb5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="11bb5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11bb5-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11bb5-124">-Name</span></span>
<span data-ttu-id="11bb5-125">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="11bb5-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bb5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11bb5-126">-ResourceGroupName</span></span>
<span data-ttu-id="11bb5-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11bb5-127">The name of the resource group.</span></span>
<span data-ttu-id="11bb5-128">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="11bb5-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="11bb5-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11bb5-129">-SubscriptionId</span></span>
<span data-ttu-id="11bb5-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="11bb5-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="11bb5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bb5-131">CommonParameters</span></span>
<span data-ttu-id="11bb5-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11bb5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bb5-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11bb5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bb5-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11bb5-134">INPUTS</span></span>

### <span data-ttu-id="11bb5-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="11bb5-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="11bb5-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11bb5-136">OUTPUTS</span></span>

### <span data-ttu-id="11bb5-137">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="11bb5-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="11bb5-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11bb5-138">NOTES</span></span>

<span data-ttu-id="11bb5-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="11bb5-139">ALIASES</span></span>

<span data-ttu-id="11bb5-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11bb5-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11bb5-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="11bb5-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11bb5-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11bb5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11bb5-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="11bb5-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11bb5-144">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="11bb5-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="11bb5-145">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="11bb5-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="11bb5-146">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="11bb5-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="11bb5-147">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11bb5-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="11bb5-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="11bb5-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11bb5-149">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="11bb5-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="11bb5-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11bb5-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="11bb5-151">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="11bb5-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="11bb5-152">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="11bb5-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="11bb5-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="11bb5-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="11bb5-154">`[UserSessionId <String>]`: nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="11bb5-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="11bb5-155">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="11bb5-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="11bb5-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11bb5-156">RELATED LINKS</span></span>


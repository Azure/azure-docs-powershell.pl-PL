---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062791"
---
# <span data-ttu-id="e806a-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="e806a-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="e806a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e806a-102">SYNOPSIS</span></span>
<span data-ttu-id="e806a-103">Pobierz grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e806a-103">Get an application group.</span></span>

## <span data-ttu-id="e806a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e806a-104">SYNTAX</span></span>

### <span data-ttu-id="e806a-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e806a-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e806a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e806a-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e806a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e806a-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e806a-108">Lista</span><span class="sxs-lookup"><span data-stu-id="e806a-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e806a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e806a-109">DESCRIPTION</span></span>
<span data-ttu-id="e806a-110">Pobierz grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e806a-110">Get an application group.</span></span>

## <span data-ttu-id="e806a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e806a-111">EXAMPLES</span></span>

### <span data-ttu-id="e806a-112">Przykład 1: uzyskiwanie listy aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="e806a-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="e806a-113">To polecenie pobiera element Windows Virtual Application Grouping w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e806a-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="e806a-114">Przykład 2: Wyświetlanie listy pulpitów wirtualnych systemu ApplicationGroups</span><span class="sxs-lookup"><span data-stu-id="e806a-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="e806a-115">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu ApplicationGroups w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e806a-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="e806a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e806a-116">PARAMETERS</span></span>

### <span data-ttu-id="e806a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e806a-117">-DefaultProfile</span></span>
<span data-ttu-id="e806a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e806a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e806a-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="e806a-119">-Filter</span></span>
<span data-ttu-id="e806a-120">Wyrażenie filtru OData.</span><span class="sxs-lookup"><span data-stu-id="e806a-120">OData filter expression.</span></span>
<span data-ttu-id="e806a-121">Poprawne właściwości filtrowania to applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="e806a-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="e806a-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e806a-122">-InputObject</span></span>
<span data-ttu-id="e806a-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e806a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e806a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e806a-124">-Name</span></span>
<span data-ttu-id="e806a-125">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e806a-125">The name of the application group</span></span>

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

### <span data-ttu-id="e806a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e806a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e806a-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e806a-127">The name of the resource group.</span></span>
<span data-ttu-id="e806a-128">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e806a-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e806a-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e806a-129">-SubscriptionId</span></span>
<span data-ttu-id="e806a-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e806a-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e806a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e806a-131">CommonParameters</span></span>
<span data-ttu-id="e806a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e806a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e806a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e806a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e806a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e806a-134">INPUTS</span></span>

### <span data-ttu-id="e806a-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e806a-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e806a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e806a-136">OUTPUTS</span></span>

### <span data-ttu-id="e806a-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="e806a-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="e806a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e806a-138">NOTES</span></span>

<span data-ttu-id="e806a-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e806a-139">ALIASES</span></span>

<span data-ttu-id="e806a-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e806a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e806a-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e806a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e806a-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e806a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e806a-143">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e806a-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e806a-144">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e806a-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e806a-145">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="e806a-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e806a-146">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="e806a-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e806a-147">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e806a-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e806a-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e806a-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e806a-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e806a-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e806a-150">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e806a-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="e806a-151">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="e806a-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e806a-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e806a-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e806a-153">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="e806a-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e806a-154">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="e806a-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e806a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e806a-155">RELATED LINKS</span></span>


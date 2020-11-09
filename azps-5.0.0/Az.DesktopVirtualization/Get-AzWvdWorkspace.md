---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 4596900f336c10fe6c91bd62b7a14bde50efeef8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304801"
---
# <span data-ttu-id="dc248-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc248-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="dc248-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc248-102">SYNOPSIS</span></span>
<span data-ttu-id="dc248-103">Uzyskaj obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="dc248-103">Get a workspace.</span></span>

## <span data-ttu-id="dc248-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc248-104">SYNTAX</span></span>

### <span data-ttu-id="dc248-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc248-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc248-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="dc248-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc248-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc248-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc248-108">Lista</span><span class="sxs-lookup"><span data-stu-id="dc248-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc248-109">Opis</span><span class="sxs-lookup"><span data-stu-id="dc248-109">DESCRIPTION</span></span>
<span data-ttu-id="dc248-110">Uzyskaj obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="dc248-110">Get a workspace.</span></span>

## <span data-ttu-id="dc248-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc248-111">EXAMPLES</span></span>

### <span data-ttu-id="dc248-112">Przykład 1: uzyskiwanie wirtualnego pulpitu systemu Windows Worksapce według nazwy</span><span class="sxs-lookup"><span data-stu-id="dc248-112">Example 1: Get a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Get-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="dc248-113">To polecenie pobiera wirtualny obszar roboczy pulpitu systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc248-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="dc248-114">Przykład 2: Wyświetlanie listy obszarów roboczych klasyczny pulpit systemu Windows</span><span class="sxs-lookup"><span data-stu-id="dc248-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorksapce -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="dc248-115">To polecenie umożliwia wyświetlenie listy obszarów roboczych pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc248-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="dc248-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc248-116">PARAMETERS</span></span>

### <span data-ttu-id="dc248-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc248-117">-DefaultProfile</span></span>
<span data-ttu-id="dc248-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc248-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc248-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc248-119">-InputObject</span></span>
<span data-ttu-id="dc248-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="dc248-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc248-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc248-121">-Name</span></span>
<span data-ttu-id="dc248-122">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="dc248-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc248-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc248-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc248-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc248-124">The name of the resource group.</span></span>
<span data-ttu-id="dc248-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="dc248-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dc248-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dc248-126">-SubscriptionId</span></span>
<span data-ttu-id="dc248-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="dc248-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dc248-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc248-128">CommonParameters</span></span>
<span data-ttu-id="dc248-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc248-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc248-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc248-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc248-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc248-131">INPUTS</span></span>

### <span data-ttu-id="dc248-132">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="dc248-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dc248-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc248-133">OUTPUTS</span></span>

### <span data-ttu-id="dc248-134">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc248-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="dc248-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc248-135">NOTES</span></span>

<span data-ttu-id="dc248-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="dc248-136">ALIASES</span></span>

<span data-ttu-id="dc248-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc248-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc248-138">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="dc248-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc248-139">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc248-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc248-140">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="dc248-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc248-141">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="dc248-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dc248-142">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="dc248-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dc248-143">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="dc248-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dc248-144">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="dc248-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dc248-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="dc248-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc248-146">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc248-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dc248-147">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="dc248-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="dc248-148">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="dc248-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dc248-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="dc248-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dc248-150">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="dc248-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dc248-151">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="dc248-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dc248-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc248-152">RELATED LINKS</span></span>


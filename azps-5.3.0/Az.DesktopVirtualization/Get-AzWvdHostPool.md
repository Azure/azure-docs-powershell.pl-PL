---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 480c1d5517aa79ff7b3a0fa5dfa24f2ae6f4ae45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501119"
---
# <span data-ttu-id="a0877-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="a0877-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="a0877-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0877-102">SYNOPSIS</span></span>
<span data-ttu-id="a0877-103">Pobierz pulę hostów.</span><span class="sxs-lookup"><span data-stu-id="a0877-103">Get a host pool.</span></span>

## <span data-ttu-id="a0877-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0877-104">SYNTAX</span></span>

### <span data-ttu-id="a0877-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0877-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0877-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a0877-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a0877-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a0877-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0877-108">Lista</span><span class="sxs-lookup"><span data-stu-id="a0877-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0877-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a0877-109">DESCRIPTION</span></span>
<span data-ttu-id="a0877-110">Pobierz pulę hostów.</span><span class="sxs-lookup"><span data-stu-id="a0877-110">Get a host pool.</span></span>

## <span data-ttu-id="a0877-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0877-111">EXAMPLES</span></span>

### <span data-ttu-id="a0877-112">Przykład 1: uzyskiwanie wirtualnego pulpitu systemu Windows HostPool według nazwy</span><span class="sxs-lookup"><span data-stu-id="a0877-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="a0877-113">To polecenie pobiera wirtualny pulpit systemu Windows HostPool w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0877-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="a0877-114">Przykład 2: Wyświetlanie listy pulpitów wirtualnych systemu HostPools</span><span class="sxs-lookup"><span data-stu-id="a0877-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="a0877-115">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu HostPools w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0877-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="a0877-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0877-116">PARAMETERS</span></span>

### <span data-ttu-id="a0877-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0877-117">-DefaultProfile</span></span>
<span data-ttu-id="a0877-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0877-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0877-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0877-119">-InputObject</span></span>
<span data-ttu-id="a0877-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a0877-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0877-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0877-121">-Name</span></span>
<span data-ttu-id="a0877-122">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a0877-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a0877-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0877-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0877-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0877-124">The name of the resource group.</span></span>
<span data-ttu-id="a0877-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a0877-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a0877-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a0877-126">-SubscriptionId</span></span>
<span data-ttu-id="a0877-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a0877-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a0877-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0877-128">CommonParameters</span></span>
<span data-ttu-id="a0877-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0877-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0877-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0877-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0877-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0877-131">INPUTS</span></span>

### <span data-ttu-id="a0877-132">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a0877-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a0877-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0877-133">OUTPUTS</span></span>

### <span data-ttu-id="a0877-134">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="a0877-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="a0877-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0877-135">NOTES</span></span>

<span data-ttu-id="a0877-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a0877-136">ALIASES</span></span>

<span data-ttu-id="a0877-137">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0877-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0877-138">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a0877-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0877-139">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0877-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0877-140">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a0877-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0877-141">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0877-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a0877-142">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0877-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a0877-143">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="a0877-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a0877-144">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a0877-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a0877-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a0877-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0877-146">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="a0877-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a0877-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0877-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a0877-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a0877-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="a0877-149">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="a0877-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a0877-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a0877-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a0877-151">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="a0877-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a0877-152">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a0877-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a0877-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0877-153">RELATED LINKS</span></span>


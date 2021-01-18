---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: de52995d5cda17e332c137966f58b349d64c01f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499285"
---
# <span data-ttu-id="596c8-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="596c8-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="596c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="596c8-102">SYNOPSIS</span></span>
<span data-ttu-id="596c8-103">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="596c8-103">Get a desktop.</span></span>

## <span data-ttu-id="596c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="596c8-104">SYNTAX</span></span>

### <span data-ttu-id="596c8-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="596c8-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="596c8-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="596c8-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="596c8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="596c8-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="596c8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="596c8-108">DESCRIPTION</span></span>
<span data-ttu-id="596c8-109">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="596c8-109">Get a desktop.</span></span>

## <span data-ttu-id="596c8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="596c8-110">EXAMPLES</span></span>

### <span data-ttu-id="596c8-111">Przykład 1: uzyskiwanie pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="596c8-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="596c8-112">To polecenie pobiera pulpit pulpitu wirtualnego systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="596c8-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="596c8-113">Przykład 2: Wyświetlanie pulpitów pulpitów wirtualnych systemu Windows</span><span class="sxs-lookup"><span data-stu-id="596c8-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="596c8-114">To polecenie listsWindows pulpity pulpitów wirtualnych w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="596c8-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="596c8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="596c8-115">PARAMETERS</span></span>

### <span data-ttu-id="596c8-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="596c8-116">-ApplicationGroupName</span></span>
<span data-ttu-id="596c8-117">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="596c8-117">The name of the application group</span></span>

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

### <span data-ttu-id="596c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596c8-118">-DefaultProfile</span></span>
<span data-ttu-id="596c8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="596c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="596c8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="596c8-120">-InputObject</span></span>
<span data-ttu-id="596c8-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="596c8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="596c8-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="596c8-122">-Name</span></span>
<span data-ttu-id="596c8-123">Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="596c8-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="596c8-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="596c8-125">The name of the resource group.</span></span>
<span data-ttu-id="596c8-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="596c8-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="596c8-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="596c8-127">-SubscriptionId</span></span>
<span data-ttu-id="596c8-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="596c8-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="596c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596c8-129">CommonParameters</span></span>
<span data-ttu-id="596c8-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596c8-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="596c8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596c8-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="596c8-132">INPUTS</span></span>

### <span data-ttu-id="596c8-133">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="596c8-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="596c8-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="596c8-134">OUTPUTS</span></span>

### <span data-ttu-id="596c8-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="596c8-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="596c8-136">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="596c8-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="596c8-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="596c8-137">NOTES</span></span>

<span data-ttu-id="596c8-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="596c8-138">ALIASES</span></span>

<span data-ttu-id="596c8-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="596c8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="596c8-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="596c8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="596c8-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="596c8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="596c8-142">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="596c8-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="596c8-143">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="596c8-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="596c8-144">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="596c8-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="596c8-145">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="596c8-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="596c8-146">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="596c8-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="596c8-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="596c8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="596c8-148">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="596c8-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="596c8-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="596c8-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="596c8-150">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="596c8-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="596c8-151">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="596c8-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="596c8-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="596c8-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="596c8-153">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="596c8-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="596c8-154">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="596c8-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="596c8-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="596c8-155">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064141"
---
# <span data-ttu-id="b1f21-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="b1f21-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="b1f21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1f21-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f21-103">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="b1f21-103">Get a desktop.</span></span>

## <span data-ttu-id="b1f21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1f21-104">SYNTAX</span></span>

### <span data-ttu-id="b1f21-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b1f21-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1f21-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b1f21-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b1f21-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1f21-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1f21-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b1f21-108">DESCRIPTION</span></span>
<span data-ttu-id="b1f21-109">Pobierz pulpit.</span><span class="sxs-lookup"><span data-stu-id="b1f21-109">Get a desktop.</span></span>

## <span data-ttu-id="b1f21-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1f21-110">EXAMPLES</span></span>

### <span data-ttu-id="b1f21-111">Przykład 1: uzyskiwanie pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="b1f21-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b1f21-112">To polecenie pobiera pulpit pulpitu wirtualnego systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="b1f21-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="b1f21-113">Przykład 2: Wyświetlanie pulpitów pulpitów wirtualnych systemu Windows</span><span class="sxs-lookup"><span data-stu-id="b1f21-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="b1f21-114">To polecenie listsWindows pulpity pulpitów wirtualnych w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="b1f21-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="b1f21-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1f21-115">PARAMETERS</span></span>

### <span data-ttu-id="b1f21-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f21-116">-ApplicationGroupName</span></span>
<span data-ttu-id="b1f21-117">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b1f21-117">The name of the application group</span></span>

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

### <span data-ttu-id="b1f21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f21-118">-DefaultProfile</span></span>
<span data-ttu-id="b1f21-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f21-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f21-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b1f21-120">-InputObject</span></span>
<span data-ttu-id="b1f21-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b1f21-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1f21-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1f21-122">-Name</span></span>
<span data-ttu-id="b1f21-123">Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="b1f21-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="b1f21-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f21-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1f21-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1f21-125">The name of the resource group.</span></span>
<span data-ttu-id="b1f21-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b1f21-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b1f21-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b1f21-127">-SubscriptionId</span></span>
<span data-ttu-id="b1f21-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b1f21-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b1f21-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f21-129">CommonParameters</span></span>
<span data-ttu-id="b1f21-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f21-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f21-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1f21-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f21-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1f21-132">INPUTS</span></span>

### <span data-ttu-id="b1f21-133">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b1f21-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b1f21-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1f21-134">OUTPUTS</span></span>

### <span data-ttu-id="b1f21-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="b1f21-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="b1f21-136">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="b1f21-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="b1f21-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1f21-137">NOTES</span></span>

<span data-ttu-id="b1f21-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b1f21-138">ALIASES</span></span>

<span data-ttu-id="b1f21-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1f21-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1f21-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b1f21-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1f21-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b1f21-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1f21-142">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b1f21-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1f21-143">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b1f21-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b1f21-144">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="b1f21-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b1f21-145">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="b1f21-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b1f21-146">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b1f21-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b1f21-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b1f21-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1f21-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b1f21-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b1f21-149">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b1f21-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b1f21-150">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="b1f21-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b1f21-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b1f21-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b1f21-152">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="b1f21-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b1f21-153">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b1f21-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b1f21-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1f21-154">RELATED LINKS</span></span>


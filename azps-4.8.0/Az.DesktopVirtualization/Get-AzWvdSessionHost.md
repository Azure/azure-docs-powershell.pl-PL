---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064140"
---
# <span data-ttu-id="977db-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="977db-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="977db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="977db-102">SYNOPSIS</span></span>
<span data-ttu-id="977db-103">Uzyskaj hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="977db-103">Get a session host.</span></span>

## <span data-ttu-id="977db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="977db-104">SYNTAX</span></span>

### <span data-ttu-id="977db-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="977db-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="977db-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="977db-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="977db-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="977db-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="977db-108">Opis</span><span class="sxs-lookup"><span data-stu-id="977db-108">DESCRIPTION</span></span>
<span data-ttu-id="977db-109">Uzyskaj hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="977db-109">Get a session host.</span></span>

## <span data-ttu-id="977db-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="977db-110">EXAMPLES</span></span>

### <span data-ttu-id="977db-111">Przykład 1: uzyskiwanie wirtualnego pulpitu systemu Windows SessionHost według nazwy</span><span class="sxs-lookup"><span data-stu-id="977db-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="977db-112">To polecenie pobiera wirtualny pulpit systemu Windows SessionHost w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="977db-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="977db-113">Przykład 2: Wyświetlanie listy pulpitów wirtualnych systemu SessionHosts</span><span class="sxs-lookup"><span data-stu-id="977db-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="977db-114">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu SessionHosts w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="977db-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="977db-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="977db-115">PARAMETERS</span></span>

### <span data-ttu-id="977db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977db-116">-DefaultProfile</span></span>
<span data-ttu-id="977db-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="977db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="977db-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="977db-118">-HostPoolName</span></span>
<span data-ttu-id="977db-119">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="977db-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="977db-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="977db-120">-InputObject</span></span>
<span data-ttu-id="977db-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="977db-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="977db-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="977db-122">-Name</span></span>
<span data-ttu-id="977db-123">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="977db-123">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="977db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="977db-124">-ResourceGroupName</span></span>
<span data-ttu-id="977db-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="977db-125">The name of the resource group.</span></span>
<span data-ttu-id="977db-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="977db-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="977db-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="977db-127">-SubscriptionId</span></span>
<span data-ttu-id="977db-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="977db-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="977db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977db-129">CommonParameters</span></span>
<span data-ttu-id="977db-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977db-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="977db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977db-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="977db-132">INPUTS</span></span>

### <span data-ttu-id="977db-133">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="977db-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="977db-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="977db-134">OUTPUTS</span></span>

### <span data-ttu-id="977db-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="977db-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="977db-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="977db-136">NOTES</span></span>

<span data-ttu-id="977db-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="977db-137">ALIASES</span></span>

<span data-ttu-id="977db-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="977db-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="977db-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="977db-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="977db-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="977db-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="977db-141">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="977db-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="977db-142">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="977db-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="977db-143">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="977db-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="977db-144">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="977db-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="977db-145">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="977db-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="977db-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="977db-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="977db-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="977db-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="977db-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="977db-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="977db-149">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="977db-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="977db-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="977db-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="977db-151">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="977db-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="977db-152">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="977db-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="977db-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="977db-153">RELATED LINKS</span></span>


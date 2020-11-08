---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224538"
---
# <span data-ttu-id="87503-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="87503-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="87503-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87503-102">SYNOPSIS</span></span>
<span data-ttu-id="87503-103">Aktualizowanie hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="87503-103">Update a session host.</span></span>

## <span data-ttu-id="87503-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87503-104">SYNTAX</span></span>

### <span data-ttu-id="87503-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87503-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="87503-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="87503-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87503-107">Opis</span><span class="sxs-lookup"><span data-stu-id="87503-107">DESCRIPTION</span></span>
<span data-ttu-id="87503-108">Aktualizowanie hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="87503-108">Update a session host.</span></span>

## <span data-ttu-id="87503-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87503-109">EXAMPLES</span></span>

### <span data-ttu-id="87503-110">Przykład 1: aktualizowanie SessionHost pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="87503-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="87503-111">To polecenie aktualizuje SessionHost pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="87503-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="87503-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87503-112">PARAMETERS</span></span>

### <span data-ttu-id="87503-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="87503-113">-AllowNewSession</span></span>
<span data-ttu-id="87503-114">Zezwalanie na nową sesję.</span><span class="sxs-lookup"><span data-stu-id="87503-114">Allow a new session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="87503-115">-AssignedUser</span></span>
<span data-ttu-id="87503-116">Użytkownik przypisany do SessionHost.</span><span class="sxs-lookup"><span data-stu-id="87503-116">User assigned to SessionHost.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87503-117">-DefaultProfile</span></span>
<span data-ttu-id="87503-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87503-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87503-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="87503-119">-HostPoolName</span></span>
<span data-ttu-id="87503-120">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="87503-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87503-121">-InputObject</span></span>
<span data-ttu-id="87503-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="87503-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87503-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87503-123">-Name</span></span>
<span data-ttu-id="87503-124">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="87503-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87503-125">-ResourceGroupName</span></span>
<span data-ttu-id="87503-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87503-126">The name of the resource group.</span></span>
<span data-ttu-id="87503-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="87503-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="87503-128">-SubscriptionId</span></span>
<span data-ttu-id="87503-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="87503-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87503-130">-Confirm</span></span>
<span data-ttu-id="87503-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87503-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87503-132">-WhatIf</span></span>
<span data-ttu-id="87503-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87503-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87503-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87503-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87503-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87503-135">CommonParameters</span></span>
<span data-ttu-id="87503-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87503-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87503-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87503-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87503-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87503-138">INPUTS</span></span>

### <span data-ttu-id="87503-139">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="87503-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="87503-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87503-140">OUTPUTS</span></span>

### <span data-ttu-id="87503-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="87503-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="87503-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87503-142">NOTES</span></span>

<span data-ttu-id="87503-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="87503-143">ALIASES</span></span>

<span data-ttu-id="87503-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87503-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87503-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="87503-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87503-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87503-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87503-147">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="87503-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87503-148">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="87503-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="87503-149">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="87503-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="87503-150">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="87503-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="87503-151">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="87503-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="87503-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="87503-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87503-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87503-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="87503-154">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="87503-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="87503-155">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="87503-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="87503-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="87503-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="87503-157">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="87503-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="87503-158">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="87503-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="87503-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87503-159">RELATED LINKS</span></span>


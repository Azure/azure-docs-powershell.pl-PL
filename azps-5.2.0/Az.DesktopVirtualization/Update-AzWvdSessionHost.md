---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: cdb14bfe7992d29be17ff1a576dd3a6ca8bf09b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341062"
---
# <span data-ttu-id="ff04b-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="ff04b-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="ff04b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff04b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff04b-103">Aktualizowanie hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="ff04b-103">Update a session host.</span></span>

## <span data-ttu-id="ff04b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff04b-104">SYNTAX</span></span>

### <span data-ttu-id="ff04b-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff04b-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ff04b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ff04b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ff04b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff04b-107">DESCRIPTION</span></span>
<span data-ttu-id="ff04b-108">Aktualizowanie hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="ff04b-108">Update a session host.</span></span>

## <span data-ttu-id="ff04b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff04b-109">EXAMPLES</span></span>

### <span data-ttu-id="ff04b-110">Przykład 1: aktualizowanie SessionHost pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="ff04b-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="ff04b-111">To polecenie aktualizuje SessionHost pulpitu wirtualnego systemu Windows w puli hostów.</span><span class="sxs-lookup"><span data-stu-id="ff04b-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="ff04b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff04b-112">PARAMETERS</span></span>

### <span data-ttu-id="ff04b-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="ff04b-113">-AllowNewSession</span></span>
<span data-ttu-id="ff04b-114">Zezwalanie na nową sesję.</span><span class="sxs-lookup"><span data-stu-id="ff04b-114">Allow a new session.</span></span>

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

### <span data-ttu-id="ff04b-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="ff04b-115">-AssignedUser</span></span>
<span data-ttu-id="ff04b-116">Użytkownik przypisany do SessionHost.</span><span class="sxs-lookup"><span data-stu-id="ff04b-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="ff04b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff04b-117">-DefaultProfile</span></span>
<span data-ttu-id="ff04b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff04b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff04b-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ff04b-119">-HostPoolName</span></span>
<span data-ttu-id="ff04b-120">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ff04b-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ff04b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ff04b-121">-InputObject</span></span>
<span data-ttu-id="ff04b-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ff04b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff04b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff04b-123">-Name</span></span>
<span data-ttu-id="ff04b-124">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="ff04b-124">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="ff04b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff04b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff04b-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff04b-126">The name of the resource group.</span></span>
<span data-ttu-id="ff04b-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ff04b-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ff04b-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ff04b-128">-SubscriptionId</span></span>
<span data-ttu-id="ff04b-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ff04b-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ff04b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff04b-130">-Confirm</span></span>
<span data-ttu-id="ff04b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff04b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff04b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff04b-132">-WhatIf</span></span>
<span data-ttu-id="ff04b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff04b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff04b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff04b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff04b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff04b-135">CommonParameters</span></span>
<span data-ttu-id="ff04b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff04b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff04b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff04b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff04b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff04b-138">INPUTS</span></span>

### <span data-ttu-id="ff04b-139">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ff04b-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ff04b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff04b-140">OUTPUTS</span></span>

### <span data-ttu-id="ff04b-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="ff04b-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.ISessionHost</span></span>

## <span data-ttu-id="ff04b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff04b-142">NOTES</span></span>

<span data-ttu-id="ff04b-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ff04b-143">ALIASES</span></span>

<span data-ttu-id="ff04b-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff04b-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff04b-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ff04b-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff04b-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff04b-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff04b-147">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ff04b-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff04b-148">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ff04b-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ff04b-149">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="ff04b-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ff04b-150">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="ff04b-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ff04b-151">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ff04b-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ff04b-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ff04b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff04b-153">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="ff04b-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ff04b-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff04b-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ff04b-155">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ff04b-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="ff04b-156">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="ff04b-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ff04b-157">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ff04b-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ff04b-158">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="ff04b-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ff04b-159">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="ff04b-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ff04b-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff04b-160">RELATED LINKS</span></span>


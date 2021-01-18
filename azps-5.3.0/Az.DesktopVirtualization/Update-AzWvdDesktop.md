---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 31a9ecc324938ae3518887d58ac2a762b374328c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499246"
---
# <span data-ttu-id="030e5-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="030e5-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="030e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="030e5-102">SYNOPSIS</span></span>
<span data-ttu-id="030e5-103">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="030e5-103">Update a desktop.</span></span>

## <span data-ttu-id="030e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="030e5-104">SYNTAX</span></span>

### <span data-ttu-id="030e5-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="030e5-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="030e5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="030e5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="030e5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="030e5-107">DESCRIPTION</span></span>
<span data-ttu-id="030e5-108">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="030e5-108">Update a desktop.</span></span>

## <span data-ttu-id="030e5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="030e5-109">EXAMPLES</span></span>

### <span data-ttu-id="030e5-110">Przykład 1: aktualizowanie pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="030e5-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="030e5-111">To polecenie aktualizuje pulpit pulpitu wirtualnego systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="030e5-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="030e5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="030e5-112">PARAMETERS</span></span>

### <span data-ttu-id="030e5-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="030e5-113">-ApplicationGroupName</span></span>
<span data-ttu-id="030e5-114">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="030e5-114">The name of the application group</span></span>

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

### <span data-ttu-id="030e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030e5-115">-DefaultProfile</span></span>
<span data-ttu-id="030e5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="030e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="030e5-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="030e5-117">-Description</span></span>
<span data-ttu-id="030e5-118">Opis pulpitu.</span><span class="sxs-lookup"><span data-stu-id="030e5-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="030e5-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="030e5-119">-FriendlyName</span></span>
<span data-ttu-id="030e5-120">Przyjazna nazwa pulpitu.</span><span class="sxs-lookup"><span data-stu-id="030e5-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="030e5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="030e5-121">-InputObject</span></span>
<span data-ttu-id="030e5-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="030e5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="030e5-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="030e5-123">-Name</span></span>
<span data-ttu-id="030e5-124">Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="030e5-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="030e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="030e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="030e5-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="030e5-126">The name of the resource group.</span></span>
<span data-ttu-id="030e5-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="030e5-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="030e5-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="030e5-128">-SubscriptionId</span></span>
<span data-ttu-id="030e5-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="030e5-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="030e5-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="030e5-130">-Tag</span></span>
<span data-ttu-id="030e5-131">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="030e5-131">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="030e5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="030e5-132">-Confirm</span></span>
<span data-ttu-id="030e5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="030e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="030e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="030e5-134">-WhatIf</span></span>
<span data-ttu-id="030e5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="030e5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="030e5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="030e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="030e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030e5-137">CommonParameters</span></span>
<span data-ttu-id="030e5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="030e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030e5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="030e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030e5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="030e5-140">INPUTS</span></span>

### <span data-ttu-id="030e5-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="030e5-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="030e5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="030e5-142">OUTPUTS</span></span>

### <span data-ttu-id="030e5-143">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="030e5-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="030e5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="030e5-144">NOTES</span></span>

<span data-ttu-id="030e5-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="030e5-145">ALIASES</span></span>

<span data-ttu-id="030e5-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="030e5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="030e5-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="030e5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="030e5-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="030e5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="030e5-149">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="030e5-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="030e5-150">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="030e5-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="030e5-151">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="030e5-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="030e5-152">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="030e5-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="030e5-153">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="030e5-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="030e5-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="030e5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="030e5-155">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="030e5-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="030e5-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="030e5-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="030e5-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="030e5-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="030e5-158">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="030e5-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="030e5-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="030e5-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="030e5-160">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="030e5-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="030e5-161">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="030e5-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="030e5-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="030e5-162">RELATED LINKS</span></span>


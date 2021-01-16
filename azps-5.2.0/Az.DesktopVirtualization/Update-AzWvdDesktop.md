---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 3d1a822bf545cd111ef3fef19ba380f426a831c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328935"
---
# <span data-ttu-id="1c5a6-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="1c5a6-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="1c5a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5a6-103">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-103">Update a desktop.</span></span>

## <span data-ttu-id="1c5a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c5a6-104">SYNTAX</span></span>

### <span data-ttu-id="1c5a6-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c5a6-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c5a6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1c5a6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1c5a6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c5a6-107">DESCRIPTION</span></span>
<span data-ttu-id="1c5a6-108">Aktualizowanie pulpitu.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-108">Update a desktop.</span></span>

## <span data-ttu-id="1c5a6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c5a6-109">EXAMPLES</span></span>

### <span data-ttu-id="1c5a6-110">Przykład 1: aktualizowanie pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="1c5a6-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
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

<span data-ttu-id="1c5a6-111">To polecenie aktualizuje pulpit pulpitu wirtualnego systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="1c5a6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c5a6-112">PARAMETERS</span></span>

### <span data-ttu-id="1c5a6-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="1c5a6-113">-ApplicationGroupName</span></span>
<span data-ttu-id="1c5a6-114">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1c5a6-114">The name of the application group</span></span>

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

### <span data-ttu-id="1c5a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5a6-115">-DefaultProfile</span></span>
<span data-ttu-id="1c5a6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c5a6-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="1c5a6-117">-Description</span></span>
<span data-ttu-id="1c5a6-118">Opis pulpitu.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="1c5a6-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1c5a6-119">-FriendlyName</span></span>
<span data-ttu-id="1c5a6-120">Przyjazna nazwa pulpitu.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="1c5a6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c5a6-121">-InputObject</span></span>
<span data-ttu-id="1c5a6-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c5a6-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c5a6-123">-Name</span></span>
<span data-ttu-id="1c5a6-124">Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="1c5a6-124">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="1c5a6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c5a6-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c5a6-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-126">The name of the resource group.</span></span>
<span data-ttu-id="1c5a6-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1c5a6-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1c5a6-128">-SubscriptionId</span></span>
<span data-ttu-id="1c5a6-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1c5a6-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c5a6-130">-Tag</span></span>
<span data-ttu-id="1c5a6-131">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="1c5a6-131">tags to be updated</span></span>

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

### <span data-ttu-id="1c5a6-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c5a6-132">-Confirm</span></span>
<span data-ttu-id="1c5a6-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c5a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c5a6-134">-WhatIf</span></span>
<span data-ttu-id="1c5a6-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c5a6-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c5a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5a6-137">CommonParameters</span></span>
<span data-ttu-id="1c5a6-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5a6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c5a6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5a6-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c5a6-140">INPUTS</span></span>

### <span data-ttu-id="1c5a6-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1c5a6-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1c5a6-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c5a6-142">OUTPUTS</span></span>

### <span data-ttu-id="1c5a6-143">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="1c5a6-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IDesktop</span></span>

## <span data-ttu-id="1c5a6-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c5a6-144">NOTES</span></span>

<span data-ttu-id="1c5a6-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1c5a6-145">ALIASES</span></span>

<span data-ttu-id="1c5a6-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c5a6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c5a6-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c5a6-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c5a6-149">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1c5a6-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c5a6-150">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1c5a6-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1c5a6-151">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="1c5a6-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1c5a6-152">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="1c5a6-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1c5a6-153">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="1c5a6-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1c5a6-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1c5a6-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c5a6-155">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="1c5a6-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="1c5a6-156">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1c5a6-157">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="1c5a6-158">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="1c5a6-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1c5a6-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="1c5a6-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1c5a6-160">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="1c5a6-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1c5a6-161">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="1c5a6-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1c5a6-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c5a6-162">RELATED LINKS</span></span>


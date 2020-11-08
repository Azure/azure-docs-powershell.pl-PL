---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231955"
---
# <span data-ttu-id="4778e-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4778e-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4778e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4778e-102">SYNOPSIS</span></span>
<span data-ttu-id="4778e-103">Aktualizowanie obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4778e-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="4778e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4778e-104">SYNTAX</span></span>

### <span data-ttu-id="4778e-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4778e-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4778e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4778e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4778e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4778e-107">DESCRIPTION</span></span>
<span data-ttu-id="4778e-108">Aktualizowanie obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4778e-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="4778e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4778e-109">EXAMPLES</span></span>

### <span data-ttu-id="4778e-110">Przykład 1: Tworzenie okna aplikacji klasycznego pulpitu systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="4778e-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="4778e-111">To polecenie powoduje utworzenie grupy aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4778e-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="4778e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4778e-112">PARAMETERS</span></span>

### <span data-ttu-id="4778e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4778e-113">-DefaultProfile</span></span>
<span data-ttu-id="4778e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4778e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4778e-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="4778e-115">-Description</span></span>
<span data-ttu-id="4778e-116">Opis aplikacji ApplicationName.</span><span class="sxs-lookup"><span data-stu-id="4778e-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4778e-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4778e-117">-FriendlyName</span></span>
<span data-ttu-id="4778e-118">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4778e-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4778e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4778e-119">-InputObject</span></span>
<span data-ttu-id="4778e-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4778e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4778e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4778e-121">-Name</span></span>
<span data-ttu-id="4778e-122">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4778e-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4778e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4778e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4778e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4778e-124">The name of the resource group.</span></span>
<span data-ttu-id="4778e-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4778e-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4778e-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4778e-126">-SubscriptionId</span></span>
<span data-ttu-id="4778e-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4778e-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4778e-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="4778e-128">-Tag</span></span>
<span data-ttu-id="4778e-129">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="4778e-129">tags to be updated</span></span>

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

### <span data-ttu-id="4778e-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4778e-130">-Confirm</span></span>
<span data-ttu-id="4778e-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4778e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4778e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4778e-132">-WhatIf</span></span>
<span data-ttu-id="4778e-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4778e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4778e-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4778e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4778e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4778e-135">CommonParameters</span></span>
<span data-ttu-id="4778e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4778e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4778e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4778e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4778e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4778e-138">INPUTS</span></span>

### <span data-ttu-id="4778e-139">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4778e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4778e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4778e-140">OUTPUTS</span></span>

### <span data-ttu-id="4778e-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4778e-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="4778e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4778e-142">NOTES</span></span>

<span data-ttu-id="4778e-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4778e-143">ALIASES</span></span>

<span data-ttu-id="4778e-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4778e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4778e-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4778e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4778e-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4778e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4778e-147">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4778e-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4778e-148">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4778e-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4778e-149">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="4778e-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4778e-150">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="4778e-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4778e-151">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4778e-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4778e-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4778e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4778e-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4778e-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4778e-154">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4778e-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="4778e-155">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="4778e-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4778e-156">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4778e-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4778e-157">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="4778e-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4778e-158">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="4778e-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4778e-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4778e-159">RELATED LINKS</span></span>


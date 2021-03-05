---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 61e1eb1f5ae3846ce2f0cf7ad82d17d613d27e0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966202"
---
# <span data-ttu-id="4208e-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="4208e-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="4208e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4208e-102">SYNOPSIS</span></span>
<span data-ttu-id="4208e-103">Odłączanie sesji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4208e-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="4208e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4208e-104">SYNTAX</span></span>

### <span data-ttu-id="4208e-105">Rozłącz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4208e-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4208e-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4208e-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4208e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4208e-107">DESCRIPTION</span></span>
<span data-ttu-id="4208e-108">Odłączanie sesji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4208e-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="4208e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4208e-109">EXAMPLES</span></span>

### <span data-ttu-id="4208e-110">Przykład 1. Odłączanie użytkownika pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="4208e-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="4208e-111">To polecenie odłącza użytkownika pulpitu wirtualnego systemu Windows na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="4208e-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="4208e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4208e-112">PARAMETERS</span></span>

### <span data-ttu-id="4208e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4208e-113">-DefaultProfile</span></span>
<span data-ttu-id="4208e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4208e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4208e-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4208e-115">-HostPoolName</span></span>
<span data-ttu-id="4208e-116">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4208e-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4208e-117">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="4208e-117">-Id</span></span>
<span data-ttu-id="4208e-118">Nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="4208e-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4208e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4208e-119">-InputObject</span></span>
<span data-ttu-id="4208e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4208e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4208e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4208e-121">-PassThru</span></span>
<span data-ttu-id="4208e-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="4208e-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4208e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4208e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4208e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4208e-124">The name of the resource group.</span></span>
<span data-ttu-id="4208e-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4208e-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4208e-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="4208e-126">-SessionHostName</span></span>
<span data-ttu-id="4208e-127">Nazwa hosta sesji w określonej puli hosta</span><span class="sxs-lookup"><span data-stu-id="4208e-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4208e-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4208e-128">-SubscriptionId</span></span>
<span data-ttu-id="4208e-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4208e-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4208e-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4208e-130">-Confirm</span></span>
<span data-ttu-id="4208e-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4208e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4208e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4208e-132">-WhatIf</span></span>
<span data-ttu-id="4208e-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4208e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4208e-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4208e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4208e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4208e-135">CommonParameters</span></span>
<span data-ttu-id="4208e-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4208e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4208e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4208e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4208e-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4208e-138">INPUTS</span></span>

### <span data-ttu-id="4208e-139">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4208e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4208e-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4208e-140">OUTPUTS</span></span>

### <span data-ttu-id="4208e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4208e-141">System.Boolean</span></span>

## <span data-ttu-id="4208e-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4208e-142">NOTES</span></span>

<span data-ttu-id="4208e-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4208e-143">ALIASES</span></span>

<span data-ttu-id="4208e-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4208e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4208e-145">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4208e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4208e-146">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4208e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4208e-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4208e-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4208e-148">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4208e-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4208e-149">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4208e-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4208e-150">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="4208e-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4208e-151">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4208e-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4208e-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4208e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4208e-153">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="4208e-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4208e-154">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4208e-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4208e-155">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4208e-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="4208e-156">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="4208e-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4208e-157">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4208e-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4208e-158">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="4208e-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4208e-159">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="4208e-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4208e-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4208e-160">RELATED LINKS</span></span>


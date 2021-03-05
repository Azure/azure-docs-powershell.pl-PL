---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 1976c5750b5372cedce8ccf237fe8a444fa1feee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966010"
---
# <span data-ttu-id="6fe8a-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="6fe8a-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="6fe8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe8a-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe8a-103">Wysyłanie wiadomości do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-103">Send a message to a user.</span></span>

## <span data-ttu-id="6fe8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fe8a-104">SYNTAX</span></span>

### <span data-ttu-id="6fe8a-105">SendExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="6fe8a-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6fe8a-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6fe8a-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6fe8a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fe8a-107">DESCRIPTION</span></span>
<span data-ttu-id="6fe8a-108">Wysyłanie wiadomości do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-108">Send a message to a user.</span></span>

## <span data-ttu-id="6fe8a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fe8a-109">EXAMPLES</span></span>

### <span data-ttu-id="6fe8a-110">Przykład 1. Wysyłanie wiadomości do usługi UserSession</span><span class="sxs-lookup"><span data-stu-id="6fe8a-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="6fe8a-111">To polecenie wysyła wiadomość do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="6fe8a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe8a-112">PARAMETERS</span></span>

### <span data-ttu-id="6fe8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe8a-113">-DefaultProfile</span></span>
<span data-ttu-id="6fe8a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe8a-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6fe8a-115">-HostPoolName</span></span>
<span data-ttu-id="6fe8a-116">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6fe8a-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe8a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fe8a-117">-InputObject</span></span>
<span data-ttu-id="6fe8a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe8a-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="6fe8a-119">-MessageBody</span></span>
<span data-ttu-id="6fe8a-120">Treść wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-120">Body of message.</span></span>

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

### <span data-ttu-id="6fe8a-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="6fe8a-121">-MessageTitle</span></span>
<span data-ttu-id="6fe8a-122">Tytuł wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-122">Title of message.</span></span>

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

### <span data-ttu-id="6fe8a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fe8a-123">-PassThru</span></span>
<span data-ttu-id="6fe8a-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6fe8a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe8a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6fe8a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-126">The name of the resource group.</span></span>
<span data-ttu-id="6fe8a-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe8a-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="6fe8a-128">-SessionHostName</span></span>
<span data-ttu-id="6fe8a-129">Nazwa hosta sesji w określonej puli hosta</span><span class="sxs-lookup"><span data-stu-id="6fe8a-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe8a-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fe8a-130">-SubscriptionId</span></span>
<span data-ttu-id="6fe8a-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe8a-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="6fe8a-132">-UserSessionId</span></span>
<span data-ttu-id="6fe8a-133">Nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="6fe8a-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe8a-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fe8a-134">-Confirm</span></span>
<span data-ttu-id="6fe8a-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe8a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe8a-136">-WhatIf</span></span>
<span data-ttu-id="6fe8a-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe8a-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe8a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe8a-139">CommonParameters</span></span>
<span data-ttu-id="6fe8a-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe8a-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fe8a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe8a-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe8a-142">INPUTS</span></span>

### <span data-ttu-id="6fe8a-143">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6fe8a-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6fe8a-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe8a-144">OUTPUTS</span></span>

### <span data-ttu-id="6fe8a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6fe8a-145">System.Boolean</span></span>

## <span data-ttu-id="6fe8a-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fe8a-146">NOTES</span></span>

<span data-ttu-id="6fe8a-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6fe8a-147">ALIASES</span></span>

<span data-ttu-id="6fe8a-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fe8a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6fe8a-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6fe8a-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6fe8a-151">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="6fe8a-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6fe8a-152">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="6fe8a-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6fe8a-153">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6fe8a-154">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="6fe8a-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6fe8a-155">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6fe8a-156">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6fe8a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6fe8a-157">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="6fe8a-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6fe8a-158">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6fe8a-159">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="6fe8a-160">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="6fe8a-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6fe8a-161">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6fe8a-162">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="6fe8a-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6fe8a-163">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="6fe8a-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6fe8a-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fe8a-164">RELATED LINKS</span></span>


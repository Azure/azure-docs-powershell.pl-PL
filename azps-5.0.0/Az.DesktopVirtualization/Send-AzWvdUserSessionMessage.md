---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304717"
---
# <span data-ttu-id="c4505-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="c4505-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="c4505-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4505-102">SYNOPSIS</span></span>
<span data-ttu-id="c4505-103">Wyślij wiadomość do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c4505-103">Send a message to a user.</span></span>

## <span data-ttu-id="c4505-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4505-104">SYNTAX</span></span>

### <span data-ttu-id="c4505-105">SendExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4505-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c4505-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c4505-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4505-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c4505-107">DESCRIPTION</span></span>
<span data-ttu-id="c4505-108">Wyślij wiadomość do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c4505-108">Send a message to a user.</span></span>

## <span data-ttu-id="c4505-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4505-109">EXAMPLES</span></span>

### <span data-ttu-id="c4505-110">Przykład 1. Wyślij wiadomość do UserSession</span><span class="sxs-lookup"><span data-stu-id="c4505-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="c4505-111">To polecenie wysyła wiadomość do UserSession.</span><span class="sxs-lookup"><span data-stu-id="c4505-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="c4505-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4505-112">PARAMETERS</span></span>

### <span data-ttu-id="c4505-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4505-113">-DefaultProfile</span></span>
<span data-ttu-id="c4505-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4505-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4505-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c4505-115">-HostPoolName</span></span>
<span data-ttu-id="c4505-116">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c4505-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="c4505-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4505-117">-InputObject</span></span>
<span data-ttu-id="c4505-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c4505-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4505-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="c4505-119">-MessageBody</span></span>
<span data-ttu-id="c4505-120">Treść wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c4505-120">Body of message.</span></span>

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

### <span data-ttu-id="c4505-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="c4505-121">-MessageTitle</span></span>
<span data-ttu-id="c4505-122">Tytuł wiadomości.</span><span class="sxs-lookup"><span data-stu-id="c4505-122">Title of message.</span></span>

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

### <span data-ttu-id="c4505-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4505-123">-PassThru</span></span>
<span data-ttu-id="c4505-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="c4505-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4505-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4505-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4505-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4505-126">The name of the resource group.</span></span>
<span data-ttu-id="c4505-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c4505-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c4505-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="c4505-128">-SessionHostName</span></span>
<span data-ttu-id="c4505-129">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="c4505-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="c4505-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c4505-130">-SubscriptionId</span></span>
<span data-ttu-id="c4505-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c4505-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c4505-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="c4505-132">-UserSessionId</span></span>
<span data-ttu-id="c4505-133">Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="c4505-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="c4505-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4505-134">-Confirm</span></span>
<span data-ttu-id="c4505-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4505-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4505-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4505-136">-WhatIf</span></span>
<span data-ttu-id="c4505-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4505-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4505-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4505-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4505-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4505-139">CommonParameters</span></span>
<span data-ttu-id="c4505-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4505-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4505-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4505-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4505-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4505-142">INPUTS</span></span>

### <span data-ttu-id="c4505-143">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c4505-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c4505-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4505-144">OUTPUTS</span></span>

### <span data-ttu-id="c4505-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4505-145">System.Boolean</span></span>

## <span data-ttu-id="c4505-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4505-146">NOTES</span></span>

<span data-ttu-id="c4505-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c4505-147">ALIASES</span></span>

<span data-ttu-id="c4505-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4505-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4505-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c4505-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4505-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4505-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4505-151">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="c4505-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4505-152">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c4505-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c4505-153">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="c4505-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c4505-154">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="c4505-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c4505-155">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="c4505-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c4505-156">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="c4505-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4505-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4505-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4505-158">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="c4505-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4505-159">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="c4505-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c4505-160">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="c4505-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4505-161">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="c4505-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c4505-162">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="c4505-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c4505-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4505-163">RELATED LINKS</span></span>


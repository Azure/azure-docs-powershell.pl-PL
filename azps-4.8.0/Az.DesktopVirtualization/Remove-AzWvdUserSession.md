---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221223"
---
# <span data-ttu-id="b7fa7-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="b7fa7-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="b7fa7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fa7-103">Usuwanie userSession.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-103">Remove a userSession.</span></span>

## <span data-ttu-id="b7fa7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7fa7-104">SYNTAX</span></span>

### <span data-ttu-id="b7fa7-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b7fa7-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7fa7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7fa7-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7fa7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b7fa7-107">DESCRIPTION</span></span>
<span data-ttu-id="b7fa7-108">Usuwanie userSession.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-108">Remove a userSession.</span></span>

## <span data-ttu-id="b7fa7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7fa7-109">EXAMPLES</span></span>

### <span data-ttu-id="b7fa7-110">Przykład 1: usuwanie pulpitu wirtualnego systemu UserSession według nazwy</span><span class="sxs-lookup"><span data-stu-id="b7fa7-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="b7fa7-111">To polecenie usuwa UserSession pulpitu wirtualnego systemu Windows na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="b7fa7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7fa7-112">PARAMETERS</span></span>

### <span data-ttu-id="b7fa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fa7-113">-DefaultProfile</span></span>
<span data-ttu-id="b7fa7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fa7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b7fa7-115">-Force</span></span>
<span data-ttu-id="b7fa7-116">Wymuszaj flagę logowania userSession.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="b7fa7-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b7fa7-117">-HostPoolName</span></span>
<span data-ttu-id="b7fa7-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b7fa7-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fa7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="b7fa7-119">-Id</span></span>
<span data-ttu-id="b7fa7-120">Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="b7fa7-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fa7-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b7fa7-121">-InputObject</span></span>
<span data-ttu-id="b7fa7-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7fa7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7fa7-123">-PassThru</span></span>
<span data-ttu-id="b7fa7-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b7fa7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fa7-125">-ResourceGroupName</span></span>
<span data-ttu-id="b7fa7-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-126">The name of the resource group.</span></span>
<span data-ttu-id="b7fa7-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fa7-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="b7fa7-128">-SessionHostName</span></span>
<span data-ttu-id="b7fa7-129">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="b7fa7-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fa7-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b7fa7-130">-SubscriptionId</span></span>
<span data-ttu-id="b7fa7-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fa7-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7fa7-132">-Confirm</span></span>
<span data-ttu-id="b7fa7-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7fa7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7fa7-134">-WhatIf</span></span>
<span data-ttu-id="b7fa7-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7fa7-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7fa7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fa7-137">CommonParameters</span></span>
<span data-ttu-id="b7fa7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fa7-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7fa7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fa7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7fa7-140">INPUTS</span></span>

### <span data-ttu-id="b7fa7-141">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b7fa7-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b7fa7-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7fa7-142">OUTPUTS</span></span>

### <span data-ttu-id="b7fa7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7fa7-143">System.Boolean</span></span>

## <span data-ttu-id="b7fa7-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7fa7-144">NOTES</span></span>

<span data-ttu-id="b7fa7-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b7fa7-145">ALIASES</span></span>

<span data-ttu-id="b7fa7-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7fa7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7fa7-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7fa7-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7fa7-149">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b7fa7-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7fa7-150">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b7fa7-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b7fa7-151">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="b7fa7-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b7fa7-152">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="b7fa7-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b7fa7-153">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b7fa7-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b7fa7-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b7fa7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7fa7-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b7fa7-156">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="b7fa7-157">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="b7fa7-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b7fa7-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b7fa7-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b7fa7-159">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="b7fa7-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b7fa7-160">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b7fa7-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b7fa7-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7fa7-161">RELATED LINKS</span></span>


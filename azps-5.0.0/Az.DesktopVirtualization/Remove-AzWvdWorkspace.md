---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304734"
---
# <span data-ttu-id="252d6-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="252d6-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="252d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="252d6-102">SYNOPSIS</span></span>
<span data-ttu-id="252d6-103">Usuwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="252d6-103">Remove a workspace.</span></span>

## <span data-ttu-id="252d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="252d6-104">SYNTAX</span></span>

### <span data-ttu-id="252d6-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="252d6-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="252d6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="252d6-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="252d6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="252d6-107">DESCRIPTION</span></span>
<span data-ttu-id="252d6-108">Usuwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="252d6-108">Remove a workspace.</span></span>

## <span data-ttu-id="252d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="252d6-109">EXAMPLES</span></span>

### <span data-ttu-id="252d6-110">Przykład 1: usuwanie pulpitu wirtualnego systemu Worksapce według nazwy</span><span class="sxs-lookup"><span data-stu-id="252d6-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="252d6-111">To polecenie usuwa obszar roboczy pulpit wirtualny systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="252d6-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="252d6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="252d6-112">PARAMETERS</span></span>

### <span data-ttu-id="252d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252d6-113">-DefaultProfile</span></span>
<span data-ttu-id="252d6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="252d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="252d6-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="252d6-115">-InputObject</span></span>
<span data-ttu-id="252d6-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="252d6-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="252d6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="252d6-117">-Name</span></span>
<span data-ttu-id="252d6-118">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="252d6-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252d6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="252d6-119">-PassThru</span></span>
<span data-ttu-id="252d6-120">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="252d6-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="252d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="252d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="252d6-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="252d6-122">The name of the resource group.</span></span>
<span data-ttu-id="252d6-123">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="252d6-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="252d6-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="252d6-124">-SubscriptionId</span></span>
<span data-ttu-id="252d6-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="252d6-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="252d6-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="252d6-126">-Confirm</span></span>
<span data-ttu-id="252d6-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="252d6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="252d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252d6-128">-WhatIf</span></span>
<span data-ttu-id="252d6-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="252d6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="252d6-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="252d6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="252d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252d6-131">CommonParameters</span></span>
<span data-ttu-id="252d6-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252d6-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="252d6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252d6-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="252d6-134">INPUTS</span></span>

### <span data-ttu-id="252d6-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="252d6-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="252d6-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="252d6-136">OUTPUTS</span></span>

### <span data-ttu-id="252d6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="252d6-137">System.Boolean</span></span>

## <span data-ttu-id="252d6-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="252d6-138">NOTES</span></span>

<span data-ttu-id="252d6-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="252d6-139">ALIASES</span></span>

<span data-ttu-id="252d6-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="252d6-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="252d6-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="252d6-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="252d6-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="252d6-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="252d6-143">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="252d6-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="252d6-144">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="252d6-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="252d6-145">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="252d6-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="252d6-146">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="252d6-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="252d6-147">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="252d6-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="252d6-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="252d6-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="252d6-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="252d6-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="252d6-150">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="252d6-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="252d6-151">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="252d6-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="252d6-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="252d6-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="252d6-153">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="252d6-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="252d6-154">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="252d6-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="252d6-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="252d6-155">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 6c885f4962734bf1034256843258f4755a9b3b44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223973"
---
# <span data-ttu-id="0e01f-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0e01f-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="0e01f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e01f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e01f-103">Usuwanie obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0e01f-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="0e01f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e01f-104">SYNTAX</span></span>

### <span data-ttu-id="0e01f-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0e01f-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0e01f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e01f-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e01f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e01f-107">DESCRIPTION</span></span>
<span data-ttu-id="0e01f-108">Usuwanie obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0e01f-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="0e01f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e01f-109">EXAMPLES</span></span>

### <span data-ttu-id="0e01f-110">Przykład 1: Usuwanie aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="0e01f-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="0e01f-111">To polecenie powoduje usunięcie grupy aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e01f-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="0e01f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e01f-112">PARAMETERS</span></span>

### <span data-ttu-id="0e01f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e01f-113">-DefaultProfile</span></span>
<span data-ttu-id="0e01f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e01f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e01f-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e01f-115">-InputObject</span></span>
<span data-ttu-id="0e01f-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0e01f-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e01f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e01f-117">-Name</span></span>
<span data-ttu-id="0e01f-118">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="0e01f-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e01f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e01f-119">-PassThru</span></span>
<span data-ttu-id="0e01f-120">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="0e01f-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0e01f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e01f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e01f-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e01f-122">The name of the resource group.</span></span>
<span data-ttu-id="0e01f-123">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0e01f-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0e01f-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0e01f-124">-SubscriptionId</span></span>
<span data-ttu-id="0e01f-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0e01f-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0e01f-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e01f-126">-Confirm</span></span>
<span data-ttu-id="0e01f-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e01f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e01f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e01f-128">-WhatIf</span></span>
<span data-ttu-id="0e01f-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e01f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e01f-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e01f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e01f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e01f-131">CommonParameters</span></span>
<span data-ttu-id="0e01f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e01f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e01f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e01f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e01f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e01f-134">INPUTS</span></span>

### <span data-ttu-id="0e01f-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0e01f-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0e01f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e01f-136">OUTPUTS</span></span>

### <span data-ttu-id="0e01f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e01f-137">System.Boolean</span></span>

## <span data-ttu-id="0e01f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e01f-138">NOTES</span></span>

<span data-ttu-id="0e01f-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0e01f-139">ALIASES</span></span>

<span data-ttu-id="0e01f-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e01f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e01f-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0e01f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e01f-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e01f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e01f-143">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="0e01f-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e01f-144">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="0e01f-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0e01f-145">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="0e01f-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0e01f-146">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="0e01f-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0e01f-147">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="0e01f-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0e01f-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0e01f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e01f-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e01f-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0e01f-150">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="0e01f-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="0e01f-151">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="0e01f-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0e01f-152">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0e01f-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0e01f-153">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="0e01f-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0e01f-154">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="0e01f-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0e01f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e01f-155">RELATED LINKS</span></span>


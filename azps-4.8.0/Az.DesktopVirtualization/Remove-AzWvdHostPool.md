---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 7b0cdf0cbe0aecdb2e1b6829ed1ec22b1e485e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223522"
---
# <span data-ttu-id="b7fb6-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="b7fb6-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="b7fb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fb6-103">Usuwanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-103">Remove a host pool.</span></span>

## <span data-ttu-id="b7fb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7fb6-104">SYNTAX</span></span>

### <span data-ttu-id="b7fb6-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b7fb6-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7fb6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7fb6-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7fb6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b7fb6-107">DESCRIPTION</span></span>
<span data-ttu-id="b7fb6-108">Usuwanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-108">Remove a host pool.</span></span>

## <span data-ttu-id="b7fb6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7fb6-109">EXAMPLES</span></span>

### <span data-ttu-id="b7fb6-110">Przykład 1: usuwanie pulpitu wirtualnego systemu HostPool według nazwy</span><span class="sxs-lookup"><span data-stu-id="b7fb6-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="b7fb6-111">To polecenie usuwa HostPool pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="b7fb6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7fb6-112">PARAMETERS</span></span>

### <span data-ttu-id="b7fb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fb6-113">-DefaultProfile</span></span>
<span data-ttu-id="b7fb6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fb6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b7fb6-115">-Force</span></span>
<span data-ttu-id="b7fb6-116">Wymuszaj flagę usuwania sessionHost.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="b7fb6-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b7fb6-117">-InputObject</span></span>
<span data-ttu-id="b7fb6-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7fb6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7fb6-119">-Name</span></span>
<span data-ttu-id="b7fb6-120">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b7fb6-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fb6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7fb6-121">-PassThru</span></span>
<span data-ttu-id="b7fb6-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b7fb6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fb6-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7fb6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-124">The name of the resource group.</span></span>
<span data-ttu-id="b7fb6-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b7fb6-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b7fb6-126">-SubscriptionId</span></span>
<span data-ttu-id="b7fb6-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b7fb6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7fb6-128">-Confirm</span></span>
<span data-ttu-id="b7fb6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7fb6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7fb6-130">-WhatIf</span></span>
<span data-ttu-id="b7fb6-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7fb6-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7fb6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fb6-133">CommonParameters</span></span>
<span data-ttu-id="b7fb6-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fb6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7fb6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fb6-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7fb6-136">INPUTS</span></span>

### <span data-ttu-id="b7fb6-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b7fb6-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b7fb6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7fb6-138">OUTPUTS</span></span>

### <span data-ttu-id="b7fb6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7fb6-139">System.Boolean</span></span>

## <span data-ttu-id="b7fb6-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7fb6-140">NOTES</span></span>

<span data-ttu-id="b7fb6-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b7fb6-141">ALIASES</span></span>

<span data-ttu-id="b7fb6-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7fb6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7fb6-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7fb6-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7fb6-145">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b7fb6-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7fb6-146">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b7fb6-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b7fb6-147">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="b7fb6-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b7fb6-148">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="b7fb6-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b7fb6-149">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b7fb6-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b7fb6-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b7fb6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7fb6-151">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b7fb6-152">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="b7fb6-153">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="b7fb6-153">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b7fb6-154">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b7fb6-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b7fb6-155">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="b7fb6-155">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b7fb6-156">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b7fb6-156">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b7fb6-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7fb6-157">RELATED LINKS</span></span>


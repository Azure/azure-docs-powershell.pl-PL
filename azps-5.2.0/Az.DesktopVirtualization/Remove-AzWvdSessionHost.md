---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: fa480a867cbbe93a756ea38b4534818ca119c098
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341137"
---
# <span data-ttu-id="ee362-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="ee362-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="ee362-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee362-102">SYNOPSIS</span></span>
<span data-ttu-id="ee362-103">Usuwanie SessionHost.</span><span class="sxs-lookup"><span data-stu-id="ee362-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="ee362-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee362-104">SYNTAX</span></span>

### <span data-ttu-id="ee362-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ee362-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ee362-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee362-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee362-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ee362-107">DESCRIPTION</span></span>
<span data-ttu-id="ee362-108">Usuwanie SessionHost.</span><span class="sxs-lookup"><span data-stu-id="ee362-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="ee362-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee362-109">EXAMPLES</span></span>

### <span data-ttu-id="ee362-110">Przykład 1: usuwanie pulpitu wirtualnego systemu SessionHost według nazwy</span><span class="sxs-lookup"><span data-stu-id="ee362-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="ee362-111">To polecenie usuwa pulpit wirtualny systemu Windows SessionHost z puli hostów.</span><span class="sxs-lookup"><span data-stu-id="ee362-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="ee362-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee362-112">PARAMETERS</span></span>

### <span data-ttu-id="ee362-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee362-113">-DefaultProfile</span></span>
<span data-ttu-id="ee362-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee362-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee362-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ee362-115">-Force</span></span>
<span data-ttu-id="ee362-116">Wymuszaj flagę w celu wymuszenia usunięcia sessionHost nawet wtedy, gdy userSession istnieje.</span><span class="sxs-lookup"><span data-stu-id="ee362-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="ee362-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ee362-117">-HostPoolName</span></span>
<span data-ttu-id="ee362-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ee362-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ee362-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ee362-119">-InputObject</span></span>
<span data-ttu-id="ee362-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ee362-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee362-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee362-121">-Name</span></span>
<span data-ttu-id="ee362-122">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="ee362-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee362-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee362-123">-PassThru</span></span>
<span data-ttu-id="ee362-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ee362-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ee362-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee362-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee362-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee362-126">The name of the resource group.</span></span>
<span data-ttu-id="ee362-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ee362-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ee362-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ee362-128">-SubscriptionId</span></span>
<span data-ttu-id="ee362-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ee362-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ee362-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee362-130">-Confirm</span></span>
<span data-ttu-id="ee362-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee362-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee362-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee362-132">-WhatIf</span></span>
<span data-ttu-id="ee362-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee362-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee362-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee362-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee362-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee362-135">CommonParameters</span></span>
<span data-ttu-id="ee362-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee362-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee362-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee362-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee362-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee362-138">INPUTS</span></span>

### <span data-ttu-id="ee362-139">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ee362-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ee362-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee362-140">OUTPUTS</span></span>

### <span data-ttu-id="ee362-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee362-141">System.Boolean</span></span>

## <span data-ttu-id="ee362-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee362-142">NOTES</span></span>

<span data-ttu-id="ee362-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ee362-143">ALIASES</span></span>

<span data-ttu-id="ee362-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee362-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee362-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ee362-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee362-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee362-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee362-147">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ee362-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee362-148">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ee362-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ee362-149">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="ee362-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ee362-150">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="ee362-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ee362-151">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ee362-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ee362-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ee362-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee362-153">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="ee362-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ee362-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee362-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ee362-155">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="ee362-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="ee362-156">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="ee362-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ee362-157">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="ee362-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ee362-158">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="ee362-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ee362-159">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="ee362-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ee362-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee362-160">RELATED LINKS</span></span>


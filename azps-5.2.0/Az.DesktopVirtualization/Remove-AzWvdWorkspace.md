---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: bd266bf6fe8a4239a1e2f10a5b462afd0fcc3577
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341101"
---
# <span data-ttu-id="4ca10-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="4ca10-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="4ca10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ca10-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca10-103">Usuwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4ca10-103">Remove a workspace.</span></span>

## <span data-ttu-id="4ca10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ca10-104">SYNTAX</span></span>

### <span data-ttu-id="4ca10-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4ca10-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ca10-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4ca10-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ca10-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4ca10-107">DESCRIPTION</span></span>
<span data-ttu-id="4ca10-108">Usuwanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4ca10-108">Remove a workspace.</span></span>

## <span data-ttu-id="4ca10-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ca10-109">EXAMPLES</span></span>

### <span data-ttu-id="4ca10-110">Przykład 1: Usuwanie obszaru roboczego pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="4ca10-110">Example 1: Delete a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="4ca10-111">To polecenie usuwa obszar roboczy pulpit wirtualny systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ca10-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="4ca10-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ca10-112">PARAMETERS</span></span>

### <span data-ttu-id="4ca10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca10-113">-DefaultProfile</span></span>
<span data-ttu-id="4ca10-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca10-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ca10-115">-InputObject</span></span>
<span data-ttu-id="4ca10-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4ca10-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ca10-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ca10-117">-Name</span></span>
<span data-ttu-id="4ca10-118">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="4ca10-118">The name of the workspace</span></span>

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

### <span data-ttu-id="4ca10-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ca10-119">-PassThru</span></span>
<span data-ttu-id="4ca10-120">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="4ca10-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4ca10-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ca10-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ca10-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ca10-122">The name of the resource group.</span></span>
<span data-ttu-id="4ca10-123">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4ca10-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4ca10-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4ca10-124">-SubscriptionId</span></span>
<span data-ttu-id="4ca10-125">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4ca10-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4ca10-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ca10-126">-Confirm</span></span>
<span data-ttu-id="4ca10-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca10-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ca10-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca10-128">-WhatIf</span></span>
<span data-ttu-id="4ca10-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca10-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ca10-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ca10-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ca10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca10-131">CommonParameters</span></span>
<span data-ttu-id="4ca10-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca10-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ca10-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca10-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ca10-134">INPUTS</span></span>

### <span data-ttu-id="4ca10-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4ca10-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4ca10-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ca10-136">OUTPUTS</span></span>

### <span data-ttu-id="4ca10-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ca10-137">System.Boolean</span></span>

## <span data-ttu-id="4ca10-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ca10-138">NOTES</span></span>

<span data-ttu-id="4ca10-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4ca10-139">ALIASES</span></span>

<span data-ttu-id="4ca10-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ca10-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ca10-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4ca10-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ca10-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ca10-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ca10-143">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4ca10-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ca10-144">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4ca10-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4ca10-145">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="4ca10-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4ca10-146">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="4ca10-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4ca10-147">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4ca10-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4ca10-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4ca10-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ca10-149">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="4ca10-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4ca10-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ca10-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4ca10-151">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4ca10-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="4ca10-152">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="4ca10-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4ca10-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4ca10-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4ca10-154">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="4ca10-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4ca10-155">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="4ca10-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4ca10-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ca10-156">RELATED LINKS</span></span>


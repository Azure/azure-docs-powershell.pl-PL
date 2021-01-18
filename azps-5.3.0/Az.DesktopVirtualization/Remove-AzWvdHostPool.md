---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 65e7d5870e03d4e2d103254aec7a44835286d5df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499257"
---
# <span data-ttu-id="bb304-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="bb304-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="bb304-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb304-102">SYNOPSIS</span></span>
<span data-ttu-id="bb304-103">Usuwanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="bb304-103">Remove a host pool.</span></span>

## <span data-ttu-id="bb304-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb304-104">SYNTAX</span></span>

### <span data-ttu-id="bb304-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="bb304-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bb304-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb304-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb304-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bb304-107">DESCRIPTION</span></span>
<span data-ttu-id="bb304-108">Usuwanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="bb304-108">Remove a host pool.</span></span>

## <span data-ttu-id="bb304-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb304-109">EXAMPLES</span></span>

### <span data-ttu-id="bb304-110">Przykład 1: usuwanie pulpitu wirtualnego systemu HostPool według nazwy</span><span class="sxs-lookup"><span data-stu-id="bb304-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="bb304-111">To polecenie usuwa HostPool pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb304-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="bb304-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb304-112">PARAMETERS</span></span>

### <span data-ttu-id="bb304-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb304-113">-DefaultProfile</span></span>
<span data-ttu-id="bb304-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb304-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb304-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bb304-115">-Force</span></span>
<span data-ttu-id="bb304-116">Wymuszaj flagę usuwania sessionHost.</span><span class="sxs-lookup"><span data-stu-id="bb304-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="bb304-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb304-117">-InputObject</span></span>
<span data-ttu-id="bb304-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="bb304-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb304-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb304-119">-Name</span></span>
<span data-ttu-id="bb304-120">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="bb304-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="bb304-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb304-121">-PassThru</span></span>
<span data-ttu-id="bb304-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="bb304-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bb304-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb304-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb304-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb304-124">The name of the resource group.</span></span>
<span data-ttu-id="bb304-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="bb304-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bb304-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bb304-126">-SubscriptionId</span></span>
<span data-ttu-id="bb304-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bb304-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bb304-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb304-128">-Confirm</span></span>
<span data-ttu-id="bb304-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb304-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb304-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb304-130">-WhatIf</span></span>
<span data-ttu-id="bb304-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb304-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb304-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb304-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb304-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb304-133">CommonParameters</span></span>
<span data-ttu-id="bb304-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb304-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb304-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb304-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb304-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb304-136">INPUTS</span></span>

### <span data-ttu-id="bb304-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="bb304-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bb304-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb304-138">OUTPUTS</span></span>

### <span data-ttu-id="bb304-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb304-139">System.Boolean</span></span>

## <span data-ttu-id="bb304-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb304-140">NOTES</span></span>

<span data-ttu-id="bb304-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="bb304-141">ALIASES</span></span>

<span data-ttu-id="bb304-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb304-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb304-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bb304-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb304-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb304-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb304-145">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="bb304-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb304-146">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="bb304-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bb304-147">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="bb304-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bb304-148">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="bb304-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bb304-149">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="bb304-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bb304-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bb304-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb304-151">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="bb304-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="bb304-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb304-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bb304-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="bb304-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="bb304-154">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="bb304-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bb304-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="bb304-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bb304-156">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="bb304-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bb304-157">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="bb304-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bb304-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb304-158">RELATED LINKS</span></span>


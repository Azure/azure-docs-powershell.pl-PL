---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501107"
---
# <span data-ttu-id="15465-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="15465-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="15465-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15465-102">SYNOPSIS</span></span>
<span data-ttu-id="15465-103">Usuwanie pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="15465-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="15465-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15465-104">SYNTAX</span></span>

### <span data-ttu-id="15465-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="15465-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="15465-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15465-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15465-107">Opis</span><span class="sxs-lookup"><span data-stu-id="15465-107">DESCRIPTION</span></span>
<span data-ttu-id="15465-108">Usuwanie pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="15465-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="15465-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15465-109">EXAMPLES</span></span>

### <span data-ttu-id="15465-110">Przykład 1: Usuwanie pakietu MSIX według pakietu pełna nazwa</span><span class="sxs-lookup"><span data-stu-id="15465-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="15465-111">To polecenie usuwa pakiet MSIX w HostPool</span><span class="sxs-lookup"><span data-stu-id="15465-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="15465-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15465-112">PARAMETERS</span></span>

### <span data-ttu-id="15465-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15465-113">-DefaultProfile</span></span>
<span data-ttu-id="15465-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15465-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15465-115">-ImięNazwisko</span><span class="sxs-lookup"><span data-stu-id="15465-115">-FullName</span></span>
<span data-ttu-id="15465-116">Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="15465-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15465-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="15465-117">-HostPoolName</span></span>
<span data-ttu-id="15465-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="15465-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="15465-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15465-119">-InputObject</span></span>
<span data-ttu-id="15465-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="15465-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15465-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15465-121">-PassThru</span></span>
<span data-ttu-id="15465-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="15465-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15465-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15465-123">-ResourceGroupName</span></span>
<span data-ttu-id="15465-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15465-124">The name of the resource group.</span></span>
<span data-ttu-id="15465-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="15465-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15465-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="15465-126">-SubscriptionId</span></span>
<span data-ttu-id="15465-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="15465-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="15465-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15465-128">-Confirm</span></span>
<span data-ttu-id="15465-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15465-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15465-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15465-130">-WhatIf</span></span>
<span data-ttu-id="15465-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15465-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15465-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15465-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15465-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15465-133">CommonParameters</span></span>
<span data-ttu-id="15465-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15465-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15465-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15465-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15465-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15465-136">INPUTS</span></span>

### <span data-ttu-id="15465-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="15465-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="15465-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15465-138">OUTPUTS</span></span>

### <span data-ttu-id="15465-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15465-139">System.Boolean</span></span>

## <span data-ttu-id="15465-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15465-140">NOTES</span></span>

<span data-ttu-id="15465-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="15465-141">ALIASES</span></span>

<span data-ttu-id="15465-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15465-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15465-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="15465-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15465-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15465-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15465-145">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="15465-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15465-146">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="15465-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="15465-147">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="15465-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="15465-148">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="15465-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="15465-149">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="15465-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="15465-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="15465-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15465-151">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="15465-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="15465-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15465-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="15465-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="15465-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="15465-154">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="15465-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="15465-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="15465-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="15465-156">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="15465-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="15465-157">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="15465-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="15465-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15465-158">RELATED LINKS</span></span>


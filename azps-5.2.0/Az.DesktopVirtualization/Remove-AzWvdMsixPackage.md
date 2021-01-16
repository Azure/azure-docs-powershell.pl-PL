---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328949"
---
# <span data-ttu-id="871e6-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="871e6-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="871e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="871e6-102">SYNOPSIS</span></span>
<span data-ttu-id="871e6-103">Usuwanie pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="871e6-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="871e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="871e6-104">SYNTAX</span></span>

### <span data-ttu-id="871e6-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="871e6-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="871e6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="871e6-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="871e6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="871e6-107">DESCRIPTION</span></span>
<span data-ttu-id="871e6-108">Usuwanie pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="871e6-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="871e6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="871e6-109">EXAMPLES</span></span>

### <span data-ttu-id="871e6-110">Przykład 1: Usuwanie pakietu MSIX według pakietu pełna nazwa</span><span class="sxs-lookup"><span data-stu-id="871e6-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="871e6-111">To polecenie usuwa pakiet MSIX w HostPool</span><span class="sxs-lookup"><span data-stu-id="871e6-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="871e6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="871e6-112">PARAMETERS</span></span>

### <span data-ttu-id="871e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871e6-113">-DefaultProfile</span></span>
<span data-ttu-id="871e6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="871e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="871e6-115">-ImięNazwisko</span><span class="sxs-lookup"><span data-stu-id="871e6-115">-FullName</span></span>
<span data-ttu-id="871e6-116">Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="871e6-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="871e6-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="871e6-117">-HostPoolName</span></span>
<span data-ttu-id="871e6-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="871e6-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="871e6-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="871e6-119">-InputObject</span></span>
<span data-ttu-id="871e6-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="871e6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="871e6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="871e6-121">-PassThru</span></span>
<span data-ttu-id="871e6-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="871e6-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="871e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="871e6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="871e6-124">The name of the resource group.</span></span>
<span data-ttu-id="871e6-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="871e6-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="871e6-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="871e6-126">-SubscriptionId</span></span>
<span data-ttu-id="871e6-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="871e6-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="871e6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="871e6-128">-Confirm</span></span>
<span data-ttu-id="871e6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="871e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="871e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="871e6-130">-WhatIf</span></span>
<span data-ttu-id="871e6-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="871e6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="871e6-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="871e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="871e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871e6-133">CommonParameters</span></span>
<span data-ttu-id="871e6-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871e6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="871e6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871e6-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="871e6-136">INPUTS</span></span>

### <span data-ttu-id="871e6-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="871e6-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="871e6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="871e6-138">OUTPUTS</span></span>

### <span data-ttu-id="871e6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="871e6-139">System.Boolean</span></span>

## <span data-ttu-id="871e6-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="871e6-140">NOTES</span></span>

<span data-ttu-id="871e6-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="871e6-141">ALIASES</span></span>

<span data-ttu-id="871e6-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="871e6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="871e6-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="871e6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="871e6-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="871e6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="871e6-145">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="871e6-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="871e6-146">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="871e6-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="871e6-147">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="871e6-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="871e6-148">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="871e6-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="871e6-149">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="871e6-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="871e6-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="871e6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="871e6-151">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="871e6-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="871e6-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="871e6-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="871e6-153">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="871e6-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="871e6-154">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="871e6-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="871e6-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="871e6-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="871e6-156">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="871e6-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="871e6-157">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="871e6-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="871e6-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="871e6-158">RELATED LINKS</span></span>


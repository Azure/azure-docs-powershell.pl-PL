---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: b47e87ef781138dabe5b2327227ee17f29e5a494
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328930"
---
# <span data-ttu-id="03170-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="03170-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="03170-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03170-102">SYNOPSIS</span></span>
<span data-ttu-id="03170-103">Zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="03170-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="03170-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03170-104">SYNTAX</span></span>

### <span data-ttu-id="03170-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03170-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="03170-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="03170-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03170-107">Opis</span><span class="sxs-lookup"><span data-stu-id="03170-107">DESCRIPTION</span></span>
<span data-ttu-id="03170-108">Zaktualizuj pakiet MSIX.</span><span class="sxs-lookup"><span data-stu-id="03170-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="03170-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03170-109">EXAMPLES</span></span>

### <span data-ttu-id="03170-110">Przykład 1: Aktualizowanie pakietu MSIX</span><span class="sxs-lookup"><span data-stu-id="03170-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="03170-111">To polecenie aktualizuje pakiet MSIX w HostPool.</span><span class="sxs-lookup"><span data-stu-id="03170-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="03170-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03170-112">PARAMETERS</span></span>

### <span data-ttu-id="03170-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03170-113">-DefaultProfile</span></span>
<span data-ttu-id="03170-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03170-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03170-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="03170-115">-DisplayName</span></span>
<span data-ttu-id="03170-116">Nazwa wyświetlana pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="03170-116">Display name for MSIX Package.</span></span>

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

### <span data-ttu-id="03170-117">-ImięNazwisko</span><span class="sxs-lookup"><span data-stu-id="03170-117">-FullName</span></span>
<span data-ttu-id="03170-118">Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="03170-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03170-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="03170-119">-HostPoolName</span></span>
<span data-ttu-id="03170-120">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="03170-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03170-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03170-121">-InputObject</span></span>
<span data-ttu-id="03170-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="03170-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03170-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="03170-123">-IsActive</span></span>
<span data-ttu-id="03170-124">Ustaw wersję pakietu jako aktywną dla hostpool.</span><span class="sxs-lookup"><span data-stu-id="03170-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="03170-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="03170-125">-IsRegularRegistration</span></span>
<span data-ttu-id="03170-126">Ustawianie trybu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="03170-126">Set Registration mode.</span></span>
<span data-ttu-id="03170-127">Regularny lub opóźniony.</span><span class="sxs-lookup"><span data-stu-id="03170-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="03170-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03170-128">-ResourceGroupName</span></span>
<span data-ttu-id="03170-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03170-129">The name of the resource group.</span></span>
<span data-ttu-id="03170-130">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="03170-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03170-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03170-131">-SubscriptionId</span></span>
<span data-ttu-id="03170-132">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="03170-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03170-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03170-133">-Confirm</span></span>
<span data-ttu-id="03170-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03170-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03170-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03170-135">-WhatIf</span></span>
<span data-ttu-id="03170-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03170-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03170-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03170-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03170-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03170-138">CommonParameters</span></span>
<span data-ttu-id="03170-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03170-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03170-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03170-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03170-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03170-141">INPUTS</span></span>

### <span data-ttu-id="03170-142">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="03170-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="03170-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03170-143">OUTPUTS</span></span>

### <span data-ttu-id="03170-144">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="03170-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="03170-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03170-145">NOTES</span></span>

<span data-ttu-id="03170-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="03170-146">ALIASES</span></span>

<span data-ttu-id="03170-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03170-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03170-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="03170-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03170-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03170-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03170-150">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="03170-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="03170-151">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="03170-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="03170-152">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="03170-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="03170-153">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="03170-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="03170-154">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="03170-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="03170-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="03170-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="03170-156">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="03170-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="03170-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03170-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="03170-158">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="03170-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="03170-159">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="03170-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="03170-160">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="03170-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="03170-161">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="03170-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="03170-162">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="03170-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="03170-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03170-163">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180763"
---
# <span data-ttu-id="6db5a-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="6db5a-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="6db5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6db5a-102">SYNOPSIS</span></span>
<span data-ttu-id="6db5a-103">Usuwanie pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="6db5a-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="6db5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6db5a-104">SYNTAX</span></span>

### <span data-ttu-id="6db5a-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="6db5a-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6db5a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6db5a-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6db5a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6db5a-107">DESCRIPTION</span></span>
<span data-ttu-id="6db5a-108">Usuwanie pakietu MSIX.</span><span class="sxs-lookup"><span data-stu-id="6db5a-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="6db5a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6db5a-109">EXAMPLES</span></span>

### <span data-ttu-id="6db5a-110">Przykład 1. Usuwanie pakietu MSIX według pełnej nazwy pakietu</span><span class="sxs-lookup"><span data-stu-id="6db5a-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="6db5a-111">To polecenie usuwa pakiet MSIX z buforu hosta</span><span class="sxs-lookup"><span data-stu-id="6db5a-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="6db5a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6db5a-112">PARAMETERS</span></span>

### <span data-ttu-id="6db5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db5a-113">-DefaultProfile</span></span>
<span data-ttu-id="6db5a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6db5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db5a-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="6db5a-115">-FullName</span></span>
<span data-ttu-id="6db5a-116">Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="6db5a-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="6db5a-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6db5a-117">-HostPoolName</span></span>
<span data-ttu-id="6db5a-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6db5a-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="6db5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db5a-119">-InputObject</span></span>
<span data-ttu-id="6db5a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6db5a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6db5a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6db5a-121">-PassThru</span></span>
<span data-ttu-id="6db5a-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6db5a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6db5a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db5a-123">-ResourceGroupName</span></span>
<span data-ttu-id="6db5a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6db5a-124">The name of the resource group.</span></span>
<span data-ttu-id="6db5a-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6db5a-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6db5a-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6db5a-126">-SubscriptionId</span></span>
<span data-ttu-id="6db5a-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6db5a-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6db5a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6db5a-128">-Confirm</span></span>
<span data-ttu-id="6db5a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6db5a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db5a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db5a-130">-WhatIf</span></span>
<span data-ttu-id="6db5a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db5a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db5a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6db5a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db5a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db5a-133">CommonParameters</span></span>
<span data-ttu-id="6db5a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db5a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db5a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6db5a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db5a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6db5a-136">INPUTS</span></span>

### <span data-ttu-id="6db5a-137">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6db5a-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6db5a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6db5a-138">OUTPUTS</span></span>

### <span data-ttu-id="6db5a-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6db5a-139">System.Boolean</span></span>

## <span data-ttu-id="6db5a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6db5a-140">NOTES</span></span>

<span data-ttu-id="6db5a-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6db5a-141">ALIASES</span></span>

<span data-ttu-id="6db5a-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6db5a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6db5a-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6db5a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6db5a-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6db5a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6db5a-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="6db5a-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6db5a-146">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="6db5a-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6db5a-147">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6db5a-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6db5a-148">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="6db5a-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6db5a-149">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6db5a-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6db5a-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6db5a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6db5a-151">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="6db5a-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6db5a-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6db5a-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6db5a-153">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="6db5a-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="6db5a-154">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="6db5a-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6db5a-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="6db5a-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6db5a-156">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="6db5a-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6db5a-157">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="6db5a-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6db5a-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6db5a-158">RELATED LINKS</span></span>


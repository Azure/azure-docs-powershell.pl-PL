---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186074"
---
# <span data-ttu-id="3ff27-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="3ff27-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="3ff27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff27-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff27-103">Rozwija i wyświetla pakiety MSIX na obrazie, mając ścieżkę obrazu.</span><span class="sxs-lookup"><span data-stu-id="3ff27-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="3ff27-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3ff27-104">SYNTAX</span></span>

### <span data-ttu-id="3ff27-105">ExpandExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="3ff27-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ff27-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="3ff27-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ff27-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3ff27-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ff27-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3ff27-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ff27-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3ff27-109">DESCRIPTION</span></span>
<span data-ttu-id="3ff27-110">Rozwija i wyświetla pakiety MSIX na obrazie przy podanej ścieżce obrazu.</span><span class="sxs-lookup"><span data-stu-id="3ff27-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="3ff27-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3ff27-111">EXAMPLES</span></span>

### <span data-ttu-id="3ff27-112">Przykład 1. Rozszerza określoną ścieżkę obrazu i pobiera metadane pakietu odnalezione w AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="3ff27-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="3ff27-113">To polecenie zwraca metadane pakietu MSIX znalezione w podanej ścieżce obrazu.</span><span class="sxs-lookup"><span data-stu-id="3ff27-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="3ff27-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ff27-114">PARAMETERS</span></span>

### <span data-ttu-id="3ff27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff27-115">-DefaultProfile</span></span>
<span data-ttu-id="3ff27-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff27-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3ff27-117">-HostPoolName</span></span>
<span data-ttu-id="3ff27-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="3ff27-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff27-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ff27-119">-InputObject</span></span>
<span data-ttu-id="3ff27-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3ff27-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff27-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="3ff27-121">-MsixImageUri</span></span>
<span data-ttu-id="3ff27-122">Reprezentuje wartość URI odwołującą się do funkcji MSIX Image To (Obraz MSIX) w celu skonstruowania, zobacz sekcję NOTES właściwości MSIXIMAGEURI i utwórz tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3ff27-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff27-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff27-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ff27-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ff27-124">The name of the resource group.</span></span>
<span data-ttu-id="3ff27-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3ff27-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff27-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ff27-126">-SubscriptionId</span></span>
<span data-ttu-id="3ff27-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3ff27-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff27-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="3ff27-128">-Uri</span></span>
<span data-ttu-id="3ff27-129">URI na obraz</span><span class="sxs-lookup"><span data-stu-id="3ff27-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff27-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ff27-130">-Confirm</span></span>
<span data-ttu-id="3ff27-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3ff27-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff27-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff27-132">-WhatIf</span></span>
<span data-ttu-id="3ff27-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ff27-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ff27-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3ff27-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff27-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff27-135">CommonParameters</span></span>
<span data-ttu-id="3ff27-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff27-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff27-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ff27-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff27-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ff27-138">INPUTS</span></span>

### <span data-ttu-id="3ff27-139">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="3ff27-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="3ff27-140">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3ff27-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3ff27-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ff27-141">OUTPUTS</span></span>

### <span data-ttu-id="3ff27-142">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="3ff27-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="3ff27-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3ff27-143">NOTES</span></span>

<span data-ttu-id="3ff27-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3ff27-144">ALIASES</span></span>

<span data-ttu-id="3ff27-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ff27-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ff27-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3ff27-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ff27-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3ff27-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ff27-148">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3ff27-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ff27-149">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3ff27-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3ff27-150">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3ff27-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3ff27-151">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="3ff27-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3ff27-152">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ff27-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3ff27-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3ff27-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ff27-154">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="3ff27-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3ff27-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ff27-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3ff27-156">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3ff27-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="3ff27-157">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="3ff27-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3ff27-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3ff27-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3ff27-159">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="3ff27-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3ff27-160">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="3ff27-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="3ff27-161">MSIXIMAGEURI: <IMsixImageUri> Reprezentuje wartość URI odwołującą się do obrazu MSIX</span><span class="sxs-lookup"><span data-stu-id="3ff27-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="3ff27-162">`[Uri <String>]`: URI na obraz</span><span class="sxs-lookup"><span data-stu-id="3ff27-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="3ff27-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ff27-163">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: f4767b87e7230727a2cf9c83af0c2aa5d03b908a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966193"
---
# <span data-ttu-id="56739-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="56739-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="56739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56739-102">SYNOPSIS</span></span>
<span data-ttu-id="56739-103">Rozwija i wyświetla pakiety MSIX na obrazie, mając ścieżkę obrazu.</span><span class="sxs-lookup"><span data-stu-id="56739-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="56739-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56739-104">SYNTAX</span></span>

### <span data-ttu-id="56739-105">ExpandExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="56739-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56739-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="56739-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56739-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56739-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56739-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="56739-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56739-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="56739-109">DESCRIPTION</span></span>
<span data-ttu-id="56739-110">Rozwija i wyświetla pakiety MSIX na obrazie, mając ścieżkę obrazu.</span><span class="sxs-lookup"><span data-stu-id="56739-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="56739-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56739-111">EXAMPLES</span></span>

### <span data-ttu-id="56739-112">Przykład 1. Rozszerza określoną ścieżkę obrazu i pobiera metadane pakietu odnalezione w AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="56739-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="56739-113">To polecenie zwraca metadane pakietu MSIX znalezione w danej ścieżce obrazu.</span><span class="sxs-lookup"><span data-stu-id="56739-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="56739-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56739-114">PARAMETERS</span></span>

### <span data-ttu-id="56739-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56739-115">-DefaultProfile</span></span>
<span data-ttu-id="56739-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56739-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56739-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="56739-117">-HostPoolName</span></span>
<span data-ttu-id="56739-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="56739-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="56739-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56739-119">-InputObject</span></span>
<span data-ttu-id="56739-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="56739-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56739-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="56739-121">-MsixImageUri</span></span>
<span data-ttu-id="56739-122">Reprezentuje wartość URI odwołującą się do funkcji MSIX Image To (Obraz MSIX) w celu skonstruowania, zobacz sekcję NOTES właściwości MSIXIMAGEURI i utwórz tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="56739-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

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

### <span data-ttu-id="56739-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56739-123">-ResourceGroupName</span></span>
<span data-ttu-id="56739-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56739-124">The name of the resource group.</span></span>
<span data-ttu-id="56739-125">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="56739-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="56739-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56739-126">-SubscriptionId</span></span>
<span data-ttu-id="56739-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="56739-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="56739-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="56739-128">-Uri</span></span>
<span data-ttu-id="56739-129">URI na obraz</span><span class="sxs-lookup"><span data-stu-id="56739-129">URI to Image</span></span>

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

### <span data-ttu-id="56739-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56739-130">-Confirm</span></span>
<span data-ttu-id="56739-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56739-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56739-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56739-132">-WhatIf</span></span>
<span data-ttu-id="56739-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56739-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56739-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="56739-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56739-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56739-135">CommonParameters</span></span>
<span data-ttu-id="56739-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56739-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56739-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56739-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56739-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56739-138">INPUTS</span></span>

### <span data-ttu-id="56739-139">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="56739-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="56739-140">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="56739-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="56739-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56739-141">OUTPUTS</span></span>

### <span data-ttu-id="56739-142">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="56739-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="56739-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56739-143">NOTES</span></span>

<span data-ttu-id="56739-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="56739-144">ALIASES</span></span>

<span data-ttu-id="56739-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56739-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56739-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="56739-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56739-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56739-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56739-148">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="56739-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56739-149">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="56739-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="56739-150">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="56739-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="56739-151">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="56739-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="56739-152">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56739-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="56739-153">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="56739-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56739-154">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="56739-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="56739-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56739-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="56739-156">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="56739-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="56739-157">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="56739-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="56739-158">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="56739-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="56739-159">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="56739-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="56739-160">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="56739-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="56739-161">MSIXIMAGEURI: <IMsixImageUri> Reprezentuje wartość URI odwołującą się do obrazu MSIX</span><span class="sxs-lookup"><span data-stu-id="56739-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="56739-162">`[Uri <String>]`: URI na obraz</span><span class="sxs-lookup"><span data-stu-id="56739-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="56739-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56739-163">RELATED LINKS</span></span>


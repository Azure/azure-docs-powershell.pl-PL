---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387312"
---
# <span data-ttu-id="47052-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="47052-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="47052-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47052-102">SYNOPSIS</span></span>
<span data-ttu-id="47052-103">Rozwija i wyświetla listę pakietów MSIX w obrazie, uwzględniając ścieżkę obrazu.</span><span class="sxs-lookup"><span data-stu-id="47052-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="47052-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47052-104">SYNTAX</span></span>

### <span data-ttu-id="47052-105">ExpandExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="47052-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47052-106">Większa</span><span class="sxs-lookup"><span data-stu-id="47052-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47052-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47052-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47052-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="47052-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47052-109">Opis</span><span class="sxs-lookup"><span data-stu-id="47052-109">DESCRIPTION</span></span>
<span data-ttu-id="47052-110">Rozwija i wyświetla listę pakietów MSIX w obrazie, uwzględniając ścieżkę obrazu.</span><span class="sxs-lookup"><span data-stu-id="47052-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="47052-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47052-111">EXAMPLES</span></span>

### <span data-ttu-id="47052-112">Przykład 1: rozwija określoną ścieżkę obrazu i pobiera metadane pakietu Znalezione w AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="47052-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="47052-113">To polecenie zwraca metadane pakietu MSIX znalezionego w podanej ścieżce obrazu.</span><span class="sxs-lookup"><span data-stu-id="47052-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="47052-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47052-114">PARAMETERS</span></span>

### <span data-ttu-id="47052-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47052-115">-DefaultProfile</span></span>
<span data-ttu-id="47052-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47052-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47052-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="47052-117">-HostPoolName</span></span>
<span data-ttu-id="47052-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="47052-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="47052-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="47052-119">-InputObject</span></span>
<span data-ttu-id="47052-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="47052-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47052-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="47052-121">-MsixImageUri</span></span>
<span data-ttu-id="47052-122">Reprezentuje identyfikator URI dotyczący MSIX obraz do skonstruowania, zobacz sekcję Uwagi dla właściwości MSIXIMAGEURI i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="47052-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

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

### <span data-ttu-id="47052-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47052-123">-ResourceGroupName</span></span>
<span data-ttu-id="47052-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47052-124">The name of the resource group.</span></span>
<span data-ttu-id="47052-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="47052-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="47052-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="47052-126">-SubscriptionId</span></span>
<span data-ttu-id="47052-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="47052-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="47052-128">-URI</span><span class="sxs-lookup"><span data-stu-id="47052-128">-Uri</span></span>
<span data-ttu-id="47052-129">Identyfikator URI do obrazu</span><span class="sxs-lookup"><span data-stu-id="47052-129">URI to Image</span></span>

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

### <span data-ttu-id="47052-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47052-130">-Confirm</span></span>
<span data-ttu-id="47052-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47052-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47052-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47052-132">-WhatIf</span></span>
<span data-ttu-id="47052-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47052-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47052-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47052-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47052-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47052-135">CommonParameters</span></span>
<span data-ttu-id="47052-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47052-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47052-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47052-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47052-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47052-138">INPUTS</span></span>

### <span data-ttu-id="47052-139">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="47052-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="47052-140">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="47052-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="47052-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47052-141">OUTPUTS</span></span>

### <span data-ttu-id="47052-142">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="47052-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="47052-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47052-143">NOTES</span></span>

<span data-ttu-id="47052-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="47052-144">ALIASES</span></span>

<span data-ttu-id="47052-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47052-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47052-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="47052-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47052-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47052-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47052-148">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="47052-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47052-149">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="47052-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="47052-150">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="47052-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="47052-151">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="47052-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="47052-152">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="47052-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="47052-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="47052-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47052-154">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="47052-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="47052-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47052-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="47052-156">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="47052-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="47052-157">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="47052-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="47052-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="47052-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="47052-159">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="47052-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="47052-160">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="47052-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="47052-161">MSIXIMAGEURI <IMsixImageUri> : reprezentuje identyfikator URI odwołujący się do obrazu MSIX</span><span class="sxs-lookup"><span data-stu-id="47052-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="47052-162">`[Uri <String>]`: Identyfikator URI do obrazu</span><span class="sxs-lookup"><span data-stu-id="47052-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="47052-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47052-163">RELATED LINKS</span></span>


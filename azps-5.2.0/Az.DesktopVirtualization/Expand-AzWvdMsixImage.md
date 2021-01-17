---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 417acf03af2bf73d57759841bacc3ed532e8f043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348157"
---
# <span data-ttu-id="df0d6-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="df0d6-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="df0d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="df0d6-103">Rozwija i wyświetla listę pakietów MSIX w obrazie, uwzględniając ścieżkę obrazu.</span><span class="sxs-lookup"><span data-stu-id="df0d6-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="df0d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df0d6-104">SYNTAX</span></span>

### <span data-ttu-id="df0d6-105">ExpandExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df0d6-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df0d6-106">Większa</span><span class="sxs-lookup"><span data-stu-id="df0d6-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df0d6-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="df0d6-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df0d6-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="df0d6-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df0d6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="df0d6-109">DESCRIPTION</span></span>
<span data-ttu-id="df0d6-110">Rozwija i wyświetla listę pakietów MSIX w obrazie, uwzględniając ścieżkę obrazu.</span><span class="sxs-lookup"><span data-stu-id="df0d6-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="df0d6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df0d6-111">EXAMPLES</span></span>

### <span data-ttu-id="df0d6-112">Przykład 1: rozwija określoną ścieżkę obrazu i pobiera metadane pakietu Znalezione w AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="df0d6-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="df0d6-113">To polecenie zwraca metadane pakietu MSIX znalezionego w podanej ścieżce obrazu.</span><span class="sxs-lookup"><span data-stu-id="df0d6-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="df0d6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df0d6-114">PARAMETERS</span></span>

### <span data-ttu-id="df0d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df0d6-115">-DefaultProfile</span></span>
<span data-ttu-id="df0d6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df0d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df0d6-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="df0d6-117">-HostPoolName</span></span>
<span data-ttu-id="df0d6-118">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="df0d6-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="df0d6-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df0d6-119">-InputObject</span></span>
<span data-ttu-id="df0d6-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="df0d6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df0d6-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="df0d6-121">-MsixImageUri</span></span>
<span data-ttu-id="df0d6-122">Reprezentuje identyfikator URI dotyczący MSIX obraz do skonstruowania, zobacz sekcję Uwagi dla właściwości MSIXIMAGEURI i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="df0d6-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df0d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df0d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="df0d6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df0d6-124">The name of the resource group.</span></span>
<span data-ttu-id="df0d6-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="df0d6-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="df0d6-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="df0d6-126">-SubscriptionId</span></span>
<span data-ttu-id="df0d6-127">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="df0d6-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="df0d6-128">-URI</span><span class="sxs-lookup"><span data-stu-id="df0d6-128">-Uri</span></span>
<span data-ttu-id="df0d6-129">Identyfikator URI do obrazu</span><span class="sxs-lookup"><span data-stu-id="df0d6-129">URI to Image</span></span>

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

### <span data-ttu-id="df0d6-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df0d6-130">-Confirm</span></span>
<span data-ttu-id="df0d6-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df0d6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df0d6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df0d6-132">-WhatIf</span></span>
<span data-ttu-id="df0d6-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df0d6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df0d6-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df0d6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df0d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0d6-135">CommonParameters</span></span>
<span data-ttu-id="df0d6-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df0d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0d6-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df0d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0d6-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df0d6-138">INPUTS</span></span>

### <span data-ttu-id="df0d6-139">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="df0d6-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri</span></span>

### <span data-ttu-id="df0d6-140">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="df0d6-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="df0d6-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df0d6-141">OUTPUTS</span></span>

### <span data-ttu-id="df0d6-142">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="df0d6-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="df0d6-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df0d6-143">NOTES</span></span>

<span data-ttu-id="df0d6-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="df0d6-144">ALIASES</span></span>

<span data-ttu-id="df0d6-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df0d6-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df0d6-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="df0d6-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df0d6-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df0d6-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df0d6-148">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="df0d6-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df0d6-149">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="df0d6-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="df0d6-150">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="df0d6-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="df0d6-151">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="df0d6-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="df0d6-152">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="df0d6-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="df0d6-153">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="df0d6-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df0d6-154">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="df0d6-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="df0d6-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df0d6-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="df0d6-156">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="df0d6-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="df0d6-157">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="df0d6-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="df0d6-158">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="df0d6-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="df0d6-159">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="df0d6-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="df0d6-160">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="df0d6-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="df0d6-161">MSIXIMAGEURI <IMsixImageUri> : reprezentuje identyfikator URI odwołujący się do obrazu MSIX</span><span class="sxs-lookup"><span data-stu-id="df0d6-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="df0d6-162">`[Uri <String>]`: Identyfikator URI do obrazu</span><span class="sxs-lookup"><span data-stu-id="df0d6-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="df0d6-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df0d6-163">RELATED LINKS</span></span>


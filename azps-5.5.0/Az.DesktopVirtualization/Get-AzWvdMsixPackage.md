---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200507"
---
# <span data-ttu-id="7ba30-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="7ba30-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="7ba30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba30-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba30-103">Pobierz pakiet msixpackage.</span><span class="sxs-lookup"><span data-stu-id="7ba30-103">Get a msixpackage.</span></span>

## <span data-ttu-id="7ba30-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ba30-104">SYNTAX</span></span>

### <span data-ttu-id="7ba30-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7ba30-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ba30-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="7ba30-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ba30-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ba30-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ba30-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ba30-108">DESCRIPTION</span></span>
<span data-ttu-id="7ba30-109">Pobierz pakiet msixpackage.</span><span class="sxs-lookup"><span data-stu-id="7ba30-109">Get a msixpackage.</span></span>

## <span data-ttu-id="7ba30-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ba30-110">EXAMPLES</span></span>

### <span data-ttu-id="7ba30-111">Przykład 1. Uzyskiwanie pakietu MSIX według nazwy</span><span class="sxs-lookup"><span data-stu-id="7ba30-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="7ba30-112">To polecenie pobiera pakiet MSIX w buforze hosta.</span><span class="sxs-lookup"><span data-stu-id="7ba30-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="7ba30-113">Przykład 2. Lista pakietów MSIX</span><span class="sxs-lookup"><span data-stu-id="7ba30-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="7ba30-114">To polecenie wyświetla listę pakietów MSIX w buforze hosta.</span><span class="sxs-lookup"><span data-stu-id="7ba30-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="7ba30-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ba30-115">PARAMETERS</span></span>

### <span data-ttu-id="7ba30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba30-116">-DefaultProfile</span></span>
<span data-ttu-id="7ba30-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba30-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="7ba30-118">-FullName</span></span>
<span data-ttu-id="7ba30-119">Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="7ba30-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba30-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="7ba30-120">-HostPoolName</span></span>
<span data-ttu-id="7ba30-121">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="7ba30-121">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba30-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ba30-122">-InputObject</span></span>
<span data-ttu-id="7ba30-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7ba30-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba30-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba30-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ba30-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ba30-125">The name of the resource group.</span></span>
<span data-ttu-id="7ba30-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="7ba30-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba30-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ba30-127">-SubscriptionId</span></span>
<span data-ttu-id="7ba30-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7ba30-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba30-129">CommonParameters</span></span>
<span data-ttu-id="7ba30-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba30-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ba30-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba30-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ba30-132">INPUTS</span></span>

### <span data-ttu-id="7ba30-133">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="7ba30-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7ba30-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ba30-134">OUTPUTS</span></span>

### <span data-ttu-id="7ba30-135">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="7ba30-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="7ba30-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ba30-136">NOTES</span></span>

<span data-ttu-id="7ba30-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7ba30-137">ALIASES</span></span>

<span data-ttu-id="7ba30-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ba30-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ba30-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7ba30-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ba30-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ba30-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ba30-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="7ba30-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ba30-142">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7ba30-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7ba30-143">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7ba30-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7ba30-144">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="7ba30-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7ba30-145">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ba30-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7ba30-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7ba30-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ba30-147">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="7ba30-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="7ba30-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ba30-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7ba30-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="7ba30-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="7ba30-150">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="7ba30-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7ba30-151">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7ba30-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7ba30-152">`[UserSessionId <String>]`: nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="7ba30-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7ba30-153">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="7ba30-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7ba30-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ba30-154">RELATED LINKS</span></span>


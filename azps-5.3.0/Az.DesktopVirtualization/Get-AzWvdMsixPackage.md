---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 51b940df2ee26c3da53c34fd7f1ffa25d3a266a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387317"
---
# <span data-ttu-id="09646-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="09646-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="09646-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09646-102">SYNOPSIS</span></span>
<span data-ttu-id="09646-103">Uzyskaj msixpackage.</span><span class="sxs-lookup"><span data-stu-id="09646-103">Get a msixpackage.</span></span>

## <span data-ttu-id="09646-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09646-104">SYNTAX</span></span>

### <span data-ttu-id="09646-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="09646-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="09646-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="09646-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="09646-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="09646-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="09646-108">Opis</span><span class="sxs-lookup"><span data-stu-id="09646-108">DESCRIPTION</span></span>
<span data-ttu-id="09646-109">Uzyskaj msixpackage.</span><span class="sxs-lookup"><span data-stu-id="09646-109">Get a msixpackage.</span></span>

## <span data-ttu-id="09646-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09646-110">EXAMPLES</span></span>

### <span data-ttu-id="09646-111">Przykład 1: Uzyskaj pakiet MSIX według nazwy</span><span class="sxs-lookup"><span data-stu-id="09646-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="09646-112">To polecenie pobiera pakiet MSIX w HostPool.</span><span class="sxs-lookup"><span data-stu-id="09646-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="09646-113">Przykład 2: lista pakietów MSIX</span><span class="sxs-lookup"><span data-stu-id="09646-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="09646-114">To polecenie wyświetla listę pakietów MSIX w HostPool.</span><span class="sxs-lookup"><span data-stu-id="09646-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="09646-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09646-115">PARAMETERS</span></span>

### <span data-ttu-id="09646-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09646-116">-DefaultProfile</span></span>
<span data-ttu-id="09646-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09646-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09646-118">-ImięNazwisko</span><span class="sxs-lookup"><span data-stu-id="09646-118">-FullName</span></span>
<span data-ttu-id="09646-119">Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="09646-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="09646-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="09646-120">-HostPoolName</span></span>
<span data-ttu-id="09646-121">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="09646-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="09646-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="09646-122">-InputObject</span></span>
<span data-ttu-id="09646-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="09646-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="09646-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09646-124">-ResourceGroupName</span></span>
<span data-ttu-id="09646-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09646-125">The name of the resource group.</span></span>
<span data-ttu-id="09646-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="09646-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="09646-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="09646-127">-SubscriptionId</span></span>
<span data-ttu-id="09646-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="09646-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="09646-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09646-129">CommonParameters</span></span>
<span data-ttu-id="09646-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09646-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09646-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09646-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09646-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09646-132">INPUTS</span></span>

### <span data-ttu-id="09646-133">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="09646-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="09646-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09646-134">OUTPUTS</span></span>

### <span data-ttu-id="09646-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="09646-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="09646-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09646-136">NOTES</span></span>

<span data-ttu-id="09646-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="09646-137">ALIASES</span></span>

<span data-ttu-id="09646-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09646-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09646-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="09646-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09646-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09646-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09646-141">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="09646-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09646-142">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="09646-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="09646-143">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="09646-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="09646-144">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="09646-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="09646-145">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="09646-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="09646-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="09646-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09646-147">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="09646-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="09646-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09646-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09646-149">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="09646-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="09646-150">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="09646-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="09646-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="09646-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09646-152">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="09646-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="09646-153">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="09646-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="09646-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09646-154">RELATED LINKS</span></span>


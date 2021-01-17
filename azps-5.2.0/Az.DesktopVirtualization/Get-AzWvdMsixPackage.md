---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 559cff58ac8d6c3f3d8f116b6147d6f4c2a4378d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330946"
---
# <span data-ttu-id="3b20b-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3b20b-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="3b20b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b20b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b20b-103">Uzyskaj msixpackage.</span><span class="sxs-lookup"><span data-stu-id="3b20b-103">Get a msixpackage.</span></span>

## <span data-ttu-id="3b20b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b20b-104">SYNTAX</span></span>

### <span data-ttu-id="3b20b-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3b20b-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3b20b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3b20b-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3b20b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3b20b-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b20b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3b20b-108">DESCRIPTION</span></span>
<span data-ttu-id="3b20b-109">Uzyskaj msixpackage.</span><span class="sxs-lookup"><span data-stu-id="3b20b-109">Get a msixpackage.</span></span>

## <span data-ttu-id="3b20b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b20b-110">EXAMPLES</span></span>

### <span data-ttu-id="3b20b-111">Przykład 1: Uzyskaj pakiet MSIX według nazwy</span><span class="sxs-lookup"><span data-stu-id="3b20b-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="3b20b-112">To polecenie pobiera pakiet MSIX w HostPool.</span><span class="sxs-lookup"><span data-stu-id="3b20b-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="3b20b-113">Przykład 2: lista pakietów MSIX</span><span class="sxs-lookup"><span data-stu-id="3b20b-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="3b20b-114">To polecenie wyświetla listę pakietów MSIX w HostPool.</span><span class="sxs-lookup"><span data-stu-id="3b20b-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="3b20b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b20b-115">PARAMETERS</span></span>

### <span data-ttu-id="3b20b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b20b-116">-DefaultProfile</span></span>
<span data-ttu-id="3b20b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b20b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b20b-118">-ImięNazwisko</span><span class="sxs-lookup"><span data-stu-id="3b20b-118">-FullName</span></span>
<span data-ttu-id="3b20b-119">Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="3b20b-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="3b20b-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3b20b-120">-HostPoolName</span></span>
<span data-ttu-id="3b20b-121">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="3b20b-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="3b20b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b20b-122">-InputObject</span></span>
<span data-ttu-id="3b20b-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3b20b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b20b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b20b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b20b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b20b-125">The name of the resource group.</span></span>
<span data-ttu-id="3b20b-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="3b20b-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3b20b-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3b20b-127">-SubscriptionId</span></span>
<span data-ttu-id="3b20b-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3b20b-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3b20b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b20b-129">CommonParameters</span></span>
<span data-ttu-id="3b20b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b20b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b20b-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b20b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b20b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b20b-132">INPUTS</span></span>

### <span data-ttu-id="3b20b-133">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3b20b-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3b20b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b20b-134">OUTPUTS</span></span>

### <span data-ttu-id="3b20b-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3b20b-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="3b20b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b20b-136">NOTES</span></span>

<span data-ttu-id="3b20b-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3b20b-137">ALIASES</span></span>

<span data-ttu-id="3b20b-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b20b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b20b-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3b20b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b20b-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b20b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b20b-141">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3b20b-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b20b-142">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3b20b-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3b20b-143">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="3b20b-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3b20b-144">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="3b20b-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3b20b-145">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="3b20b-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3b20b-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3b20b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b20b-147">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="3b20b-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3b20b-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b20b-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3b20b-149">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="3b20b-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3b20b-150">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="3b20b-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3b20b-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3b20b-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3b20b-152">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="3b20b-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3b20b-153">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="3b20b-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3b20b-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b20b-154">RELATED LINKS</span></span>


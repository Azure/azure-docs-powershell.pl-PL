---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 0bc1c5eef68abc46d43132a86afe3ab6f86b002d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341689"
---
# <span data-ttu-id="1eadd-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="1eadd-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="1eadd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1eadd-102">SYNOPSIS</span></span>
<span data-ttu-id="1eadd-103">Pobierz grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1eadd-103">Get an application group.</span></span>

## <span data-ttu-id="1eadd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1eadd-104">SYNTAX</span></span>

### <span data-ttu-id="1eadd-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1eadd-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1eadd-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1eadd-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1eadd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1eadd-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1eadd-108">Lista</span><span class="sxs-lookup"><span data-stu-id="1eadd-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1eadd-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1eadd-109">DESCRIPTION</span></span>
<span data-ttu-id="1eadd-110">Pobierz grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1eadd-110">Get an application group.</span></span>

## <span data-ttu-id="1eadd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1eadd-111">EXAMPLES</span></span>

### <span data-ttu-id="1eadd-112">Przykład 1: uzyskiwanie listy aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="1eadd-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="1eadd-113">To polecenie pobiera element Windows Virtual Application Grouping w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1eadd-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="1eadd-114">Przykład 2: Wyświetlanie listy pulpitów wirtualnych systemu ApplicationGroups</span><span class="sxs-lookup"><span data-stu-id="1eadd-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="1eadd-115">To polecenie umożliwia wyświetlenie listy pulpitów wirtualnych systemu ApplicationGroups w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1eadd-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="1eadd-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1eadd-116">PARAMETERS</span></span>

### <span data-ttu-id="1eadd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eadd-117">-DefaultProfile</span></span>
<span data-ttu-id="1eadd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1eadd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eadd-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="1eadd-119">-Filter</span></span>
<span data-ttu-id="1eadd-120">Wyrażenie filtru OData.</span><span class="sxs-lookup"><span data-stu-id="1eadd-120">OData filter expression.</span></span>
<span data-ttu-id="1eadd-121">Poprawne właściwości filtrowania to applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="1eadd-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eadd-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1eadd-122">-InputObject</span></span>
<span data-ttu-id="1eadd-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1eadd-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1eadd-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1eadd-124">-Name</span></span>
<span data-ttu-id="1eadd-125">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1eadd-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eadd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eadd-126">-ResourceGroupName</span></span>
<span data-ttu-id="1eadd-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1eadd-127">The name of the resource group.</span></span>
<span data-ttu-id="1eadd-128">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="1eadd-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1eadd-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1eadd-129">-SubscriptionId</span></span>
<span data-ttu-id="1eadd-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="1eadd-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eadd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eadd-131">CommonParameters</span></span>
<span data-ttu-id="1eadd-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eadd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eadd-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eadd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eadd-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1eadd-134">INPUTS</span></span>

### <span data-ttu-id="1eadd-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1eadd-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1eadd-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1eadd-136">OUTPUTS</span></span>

### <span data-ttu-id="1eadd-137">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="1eadd-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="1eadd-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1eadd-138">NOTES</span></span>

<span data-ttu-id="1eadd-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1eadd-139">ALIASES</span></span>

<span data-ttu-id="1eadd-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1eadd-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1eadd-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1eadd-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1eadd-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1eadd-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1eadd-143">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1eadd-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1eadd-144">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1eadd-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1eadd-145">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="1eadd-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1eadd-146">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="1eadd-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1eadd-147">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="1eadd-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1eadd-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1eadd-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1eadd-149">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="1eadd-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="1eadd-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1eadd-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1eadd-151">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="1eadd-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="1eadd-152">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="1eadd-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1eadd-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="1eadd-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1eadd-154">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="1eadd-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1eadd-155">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="1eadd-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1eadd-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1eadd-156">RELATED LINKS</span></span>


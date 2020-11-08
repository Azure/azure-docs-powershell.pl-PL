---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221239"
---
# <span data-ttu-id="e2fe5-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="e2fe5-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="e2fe5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fe5-103">Uzyskaj aplikację.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-103">Get an application.</span></span>

## <span data-ttu-id="e2fe5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2fe5-104">SYNTAX</span></span>

### <span data-ttu-id="e2fe5-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e2fe5-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2fe5-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e2fe5-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2fe5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2fe5-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2fe5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e2fe5-108">DESCRIPTION</span></span>
<span data-ttu-id="e2fe5-109">Uzyskaj aplikację.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-109">Get an application.</span></span>

## <span data-ttu-id="e2fe5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2fe5-110">EXAMPLES</span></span>

### <span data-ttu-id="e2fe5-111">Przykład 1: uzyskiwanie aplikacji klasycznej Windows przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="e2fe5-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="e2fe5-112">To polecenie pobiera wirtualną aplikację klasyczną systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="e2fe5-113">Przykład 2: Wyświetlanie listy aplikacji klasycznych dla komputerów wirtualnych systemu Windows</span><span class="sxs-lookup"><span data-stu-id="e2fe5-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="e2fe5-114">To polecenie wyświetla listę aplikacji klasycznych systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="e2fe5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2fe5-115">PARAMETERS</span></span>

### <span data-ttu-id="e2fe5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fe5-116">-DefaultProfile</span></span>
<span data-ttu-id="e2fe5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2fe5-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e2fe5-118">-GroupName</span></span>
<span data-ttu-id="e2fe5-119">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2fe5-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fe5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e2fe5-120">-InputObject</span></span>
<span data-ttu-id="e2fe5-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e2fe5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2fe5-122">-Name</span></span>
<span data-ttu-id="e2fe5-123">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2fe5-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fe5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2fe5-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2fe5-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-125">The name of the resource group.</span></span>
<span data-ttu-id="e2fe5-126">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e2fe5-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e2fe5-127">-SubscriptionId</span></span>
<span data-ttu-id="e2fe5-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e2fe5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fe5-129">CommonParameters</span></span>
<span data-ttu-id="e2fe5-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fe5-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2fe5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fe5-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2fe5-132">INPUTS</span></span>

### <span data-ttu-id="e2fe5-133">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e2fe5-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e2fe5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2fe5-134">OUTPUTS</span></span>

### <span data-ttu-id="e2fe5-135">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="e2fe5-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="e2fe5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2fe5-136">NOTES</span></span>

<span data-ttu-id="e2fe5-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e2fe5-137">ALIASES</span></span>

<span data-ttu-id="e2fe5-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2fe5-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2fe5-139">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2fe5-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2fe5-141">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="e2fe5-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2fe5-142">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2fe5-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e2fe5-143">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2fe5-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e2fe5-144">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="e2fe5-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e2fe5-145">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e2fe5-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e2fe5-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e2fe5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2fe5-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e2fe5-148">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="e2fe5-149">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="e2fe5-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e2fe5-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e2fe5-151">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="e2fe5-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e2fe5-152">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="e2fe5-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e2fe5-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2fe5-153">RELATED LINKS</span></span>


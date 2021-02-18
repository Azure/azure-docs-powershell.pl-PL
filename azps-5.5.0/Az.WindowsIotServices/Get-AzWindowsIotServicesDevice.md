---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241475"
---
# <span data-ttu-id="9e599-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="9e599-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="9e599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e599-102">SYNOPSIS</span></span>
<span data-ttu-id="9e599-103">Uzyskaj metadane niezwiązane z zabezpieczeniami usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="9e599-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="9e599-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e599-104">SYNTAX</span></span>

### <span data-ttu-id="9e599-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9e599-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e599-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="9e599-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e599-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e599-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e599-108">Lista</span><span class="sxs-lookup"><span data-stu-id="9e599-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9e599-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e599-109">DESCRIPTION</span></span>
<span data-ttu-id="9e599-110">Uzyskaj metadane niezwiązane z zabezpieczeniami usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="9e599-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="9e599-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e599-111">EXAMPLES</span></span>

### <span data-ttu-id="9e599-112">Przykład 1. Uzyskiwanie wszystkich usług IoT systemu Windows w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9e599-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="9e599-113">To polecenie pobiera wszystkie usługi IoT systemu Windows w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e599-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="9e599-114">Przykład 2. Uzyskiwanie wszystkich usług IoT systemu Windows w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="9e599-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="9e599-115">To polecenie pobiera wszystkie usługi IoT systemu Windows w ramach grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e599-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="9e599-116">Przykład 3. Uzyskiwanie usługi IoT systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="9e599-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="9e599-117">To polecenie otrzymuje usługę Windows IoT według nazwy.</span><span class="sxs-lookup"><span data-stu-id="9e599-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="9e599-118">Przykład 4. Uzyskiwanie usługi IoT systemu Windows według obiektów</span><span class="sxs-lookup"><span data-stu-id="9e599-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="9e599-119">To polecenie pobiera usługę IoT systemu Windows według obiektów.</span><span class="sxs-lookup"><span data-stu-id="9e599-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="9e599-120">Przykład 4. Uzyskiwanie usługi Windows IoT według potoku</span><span class="sxs-lookup"><span data-stu-id="9e599-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="9e599-121">To polecenie pobiera usługę IoT systemu Windows według potoku.</span><span class="sxs-lookup"><span data-stu-id="9e599-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="9e599-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e599-122">PARAMETERS</span></span>

### <span data-ttu-id="9e599-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e599-123">-DefaultProfile</span></span>
<span data-ttu-id="9e599-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e599-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e599-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e599-125">-InputObject</span></span>
<span data-ttu-id="9e599-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9e599-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e599-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9e599-127">-Name</span></span>
<span data-ttu-id="9e599-128">Nazwa usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="9e599-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e599-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e599-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e599-130">Nazwa grupy zasobów zawierającej usługę urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="9e599-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="9e599-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e599-131">-SubscriptionId</span></span>
<span data-ttu-id="9e599-132">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e599-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="9e599-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e599-133">CommonParameters</span></span>
<span data-ttu-id="9e599-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e599-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e599-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e599-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e599-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e599-136">INPUTS</span></span>

### <span data-ttu-id="9e599-137">Microsoft.Azure.PowerShell.Cmdlet.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="9e599-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="9e599-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e599-138">OUTPUTS</span></span>

### <span data-ttu-id="9e599-139">Microsoft.Azure.PowerShell.Cmdlet.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="9e599-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="9e599-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e599-140">NOTES</span></span>

<span data-ttu-id="9e599-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9e599-141">ALIASES</span></span>

<span data-ttu-id="9e599-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="9e599-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e599-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9e599-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e599-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e599-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e599-145">INPUTOBJECT: <IWindowsIotServicesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9e599-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e599-146">`[DeviceName <String>]`: nazwa usługi urządzenia z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="9e599-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="9e599-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9e599-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e599-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej usługę urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="9e599-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="9e599-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e599-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="9e599-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e599-150">RELATED LINKS</span></span>


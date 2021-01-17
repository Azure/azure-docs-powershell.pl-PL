---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491362"
---
# <span data-ttu-id="17648-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="17648-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="17648-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17648-102">SYNOPSIS</span></span>
<span data-ttu-id="17648-103">Aktualizuje metadane usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="17648-104">Typowym wzorcem do modyfikowania właściwości jest pobranie metadanych metadanych i zabezpieczeń usługi urządzenia IoT systemu Windows, a następnie połączenie ich z zmodyfikowanymi wartościami w nowej treści w celu zaktualizowania usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="17648-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17648-105">SYNTAX</span></span>

### <span data-ttu-id="17648-106">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="17648-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17648-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="17648-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="17648-108">Opis</span><span class="sxs-lookup"><span data-stu-id="17648-108">DESCRIPTION</span></span>
<span data-ttu-id="17648-109">Aktualizuje metadane usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="17648-110">Typowym wzorcem do modyfikowania właściwości jest pobranie metadanych metadanych i zabezpieczeń usługi urządzenia IoT systemu Windows, a następnie połączenie ich z zmodyfikowanymi wartościami w nowej treści w celu zaktualizowania usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="17648-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17648-111">EXAMPLES</span></span>

### <span data-ttu-id="17648-112">Przykład 1: aktualizowanie usług IoT systemu Windows według nazw</span><span class="sxs-lookup"><span data-stu-id="17648-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="17648-113">To polecenie aktualizuje usługi Windows IoT według nazwy.</span><span class="sxs-lookup"><span data-stu-id="17648-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="17648-114">Przykład 2: aktualizowanie usług IoT systemu Windows według rurociągu</span><span class="sxs-lookup"><span data-stu-id="17648-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="17648-115">To polecenie aktualizuje usługi Windows IoT według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="17648-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="17648-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17648-116">PARAMETERS</span></span>

### <span data-ttu-id="17648-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="17648-117">-AdminDomainName</span></span>
<span data-ttu-id="17648-118">Domena usługi Windows IoT Device</span><span class="sxs-lookup"><span data-stu-id="17648-118">Windows IoT Device Service OEM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="17648-119">-BillingDomainName</span></span>
<span data-ttu-id="17648-120">Domena usługi ODM w usłudze urządzenia IoT z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="17648-120">Windows IoT Device Service ODM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17648-121">-DefaultProfile</span></span>
<span data-ttu-id="17648-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17648-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17648-123">-ETag</span><span class="sxs-lookup"><span data-stu-id="17648-123">-Etag</span></span>
<span data-ttu-id="17648-124">Pole ETag *nie* jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="17648-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="17648-125">Jeśli jest podana w treści odpowiedzi, należy również podać jako nagłówek na zwykłych konwencjach ETag.</span><span class="sxs-lookup"><span data-stu-id="17648-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="17648-126">-IfMatch</span></span>
<span data-ttu-id="17648-127">Element ETag usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="17648-128">Nie określaj, czy chcesz utworzyć zupełnie nową usługę Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="17648-129">Wymagane do zaktualizowania istniejącej usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-129">Required to update an existing Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="17648-130">-InputObject</span></span>
<span data-ttu-id="17648-131">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="17648-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17648-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="17648-132">-Location</span></span>
<span data-ttu-id="17648-133">Obszar platformy Azure, w którym znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="17648-133">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17648-134">-Name</span></span>
<span data-ttu-id="17648-135">Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-136">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="17648-136">-Note</span></span>
<span data-ttu-id="17648-137">Informacje o usłudze urządzeń IoT dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="17648-137">Windows IoT Device Service notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-138">-Ilość</span><span class="sxs-lookup"><span data-stu-id="17648-138">-Quantity</span></span>
<span data-ttu-id="17648-139">Przydziały urządzeń usługi urządzenia IoT z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="17648-139">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17648-140">-ResourceGroupName</span></span>
<span data-ttu-id="17648-141">Nazwa grupy zasobów zawierającej usługę urządzenia z usługami IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="17648-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="17648-142">-SubscriptionId</span></span>
<span data-ttu-id="17648-143">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="17648-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="17648-144">-Tag</span></span>
<span data-ttu-id="17648-145">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="17648-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17648-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17648-146">-Confirm</span></span>
<span data-ttu-id="17648-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17648-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17648-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17648-148">-WhatIf</span></span>
<span data-ttu-id="17648-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17648-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17648-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17648-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17648-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17648-151">CommonParameters</span></span>
<span data-ttu-id="17648-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17648-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17648-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17648-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17648-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17648-154">INPUTS</span></span>

### <span data-ttu-id="17648-155">Microsoft. Azure. PowerShell. polecenia. WindowsIotServices. models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="17648-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="17648-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17648-156">OUTPUTS</span></span>

### <span data-ttu-id="17648-157">Microsoft. Azure. PowerShell. polecenia. WindowsIotServices. models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="17648-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="17648-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17648-158">NOTES</span></span>

<span data-ttu-id="17648-159">PISUJE</span><span class="sxs-lookup"><span data-stu-id="17648-159">ALIASES</span></span>

<span data-ttu-id="17648-160">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17648-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17648-161">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="17648-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17648-162">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17648-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17648-163">INPUTobject <IWindowsIotServicesIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="17648-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17648-164">`[DeviceName <String>]`: Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="17648-165">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="17648-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17648-166">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej usługę urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="17648-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="17648-167">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="17648-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="17648-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17648-168">RELATED LINKS</span></span>


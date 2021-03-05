---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 27eecabc9bb144270b86a26e5128b9a0d63d346b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971585"
---
# <span data-ttu-id="00007-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="00007-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="00007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00007-102">SYNOPSIS</span></span>
<span data-ttu-id="00007-103">Aktualizuje metadane usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="00007-104">Zwykłym wzorcem modyfikowania właściwości jest pobieranie metadanych i metadanych zabezpieczeń usługi IoT systemu Windows, a następnie łączenie ich z wartościami zmodyfikowanymi w nowej treści w celu zaktualizowania usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="00007-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="00007-105">SYNTAX</span></span>

### <span data-ttu-id="00007-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="00007-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="00007-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="00007-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="00007-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="00007-108">DESCRIPTION</span></span>
<span data-ttu-id="00007-109">Aktualizuje metadane usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="00007-110">Zwykłym wzorcem modyfikowania właściwości jest pobieranie metadanych i metadanych zabezpieczeń usługi IoT systemu Windows, a następnie łączenie ich z wartościami zmodyfikowanymi w nowej treści w celu zaktualizowania usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="00007-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="00007-111">EXAMPLES</span></span>

### <span data-ttu-id="00007-112">Przykład 1. Aktualizowanie usług IoT systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="00007-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="00007-113">To polecenie aktualizuje usługi IoT systemu Windows według nazwy.</span><span class="sxs-lookup"><span data-stu-id="00007-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="00007-114">Przykład 2. Aktualizowanie usług IoT systemu Windows według potoku</span><span class="sxs-lookup"><span data-stu-id="00007-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="00007-115">To polecenie aktualizuje usługi IoT systemu Windows według potoku.</span><span class="sxs-lookup"><span data-stu-id="00007-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="00007-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00007-116">PARAMETERS</span></span>

### <span data-ttu-id="00007-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="00007-117">-AdminDomainName</span></span>
<span data-ttu-id="00007-118">Domena AAD usługi OEM OEM usługi urządzeń z systemem Windows IoT</span><span class="sxs-lookup"><span data-stu-id="00007-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="00007-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="00007-119">-BillingDomainName</span></span>
<span data-ttu-id="00007-120">Domena AAD usługi urządzeń z systemem Windows IoT</span><span class="sxs-lookup"><span data-stu-id="00007-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="00007-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00007-121">-DefaultProfile</span></span>
<span data-ttu-id="00007-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="00007-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00007-123">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="00007-123">-Etag</span></span>
<span data-ttu-id="00007-124">Pole Etag nie *jest* wymagane.</span><span class="sxs-lookup"><span data-stu-id="00007-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="00007-125">Jeśli wiadomość jest dostarczana w treści odpowiedzi, musi być również zapewniana jako nagłówek zgodnie z normalną konwencją tagów ETag.</span><span class="sxs-lookup"><span data-stu-id="00007-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="00007-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="00007-126">-IfMatch</span></span>
<span data-ttu-id="00007-127">Tag ETag usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="00007-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="00007-128">Nie należy określać tworzenia zupełnie nowej usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="00007-129">Wymagane do zaktualizowania istniejącej usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="00007-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00007-130">-InputObject</span></span>
<span data-ttu-id="00007-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="00007-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="00007-132">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="00007-132">-Location</span></span>
<span data-ttu-id="00007-133">Region platformy Azure, w którym znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="00007-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="00007-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="00007-134">-Name</span></span>
<span data-ttu-id="00007-135">Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="00007-135">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="00007-136">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="00007-136">-Note</span></span>
<span data-ttu-id="00007-137">Uwagi dotyczące usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="00007-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="00007-138">— Ilość</span><span class="sxs-lookup"><span data-stu-id="00007-138">-Quantity</span></span>
<span data-ttu-id="00007-139">Alokacja urządzeń w usłudze IoT systemu Windows</span><span class="sxs-lookup"><span data-stu-id="00007-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="00007-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00007-140">-ResourceGroupName</span></span>
<span data-ttu-id="00007-141">Nazwa grupy zasobów zawierającej usługę urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="00007-142">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00007-142">-SubscriptionId</span></span>
<span data-ttu-id="00007-143">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="00007-143">The subscription identifier.</span></span>

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

### <span data-ttu-id="00007-144">— Tag</span><span class="sxs-lookup"><span data-stu-id="00007-144">-Tag</span></span>
<span data-ttu-id="00007-145">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="00007-145">Resource tags.</span></span>

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

### <span data-ttu-id="00007-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00007-146">-Confirm</span></span>
<span data-ttu-id="00007-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00007-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00007-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00007-148">-WhatIf</span></span>
<span data-ttu-id="00007-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00007-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00007-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="00007-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00007-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00007-151">CommonParameters</span></span>
<span data-ttu-id="00007-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00007-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00007-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00007-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00007-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00007-154">INPUTS</span></span>

### <span data-ttu-id="00007-155">Microsoft.Azure.PowerShell.Cmdlet.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="00007-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="00007-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00007-156">OUTPUTS</span></span>

### <span data-ttu-id="00007-157">Microsoft.Azure.PowerShell.Cmdlet.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="00007-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="00007-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="00007-158">NOTES</span></span>

<span data-ttu-id="00007-159">ALIASY</span><span class="sxs-lookup"><span data-stu-id="00007-159">ALIASES</span></span>

<span data-ttu-id="00007-160">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00007-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="00007-161">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="00007-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00007-162">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00007-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="00007-163">INPUTOBJECT: <IWindowsIotServicesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="00007-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00007-164">`[DeviceName <String>]`: nazwa usługi urządzenia z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="00007-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="00007-165">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="00007-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00007-166">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej usługę urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="00007-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="00007-167">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="00007-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="00007-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00007-168">RELATED LINKS</span></span>


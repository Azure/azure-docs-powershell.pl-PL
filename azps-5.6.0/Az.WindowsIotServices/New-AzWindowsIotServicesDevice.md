---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 40256025817e4f840f8d65ff8bdf6bc92c5b3d10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999146"
---
# <span data-ttu-id="90c31-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="90c31-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="90c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c31-102">SYNOPSIS</span></span>
<span data-ttu-id="90c31-103">Utwórz lub zaktualizuj metadane usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="90c31-104">Zwykłym wzorcem modyfikowania właściwości jest pobieranie metadanych i metadanych zabezpieczeń usługi IoT systemu Windows, a następnie łączenie ich z wartościami zmodyfikowanymi w nowej treści w celu zaktualizowania usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="90c31-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="90c31-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90c31-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="90c31-106">DESCRIPTION</span></span>
<span data-ttu-id="90c31-107">Utwórz lub zaktualizuj metadane usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="90c31-108">Zwykłym wzorcem modyfikowania właściwości jest pobieranie metadanych i metadanych zabezpieczeń usługi IoT systemu Windows, a następnie łączenie ich z wartościami zmodyfikowanymi w nowej treści w celu zaktualizowania usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="90c31-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="90c31-109">EXAMPLES</span></span>

### <span data-ttu-id="90c31-110">Przykład 1. Tworzenie nowych usług IoT systemu Windows</span><span class="sxs-lookup"><span data-stu-id="90c31-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="90c31-111">To polecenie tworzy nowe usługi IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="90c31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90c31-112">PARAMETERS</span></span>

### <span data-ttu-id="90c31-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="90c31-113">-AdminDomainName</span></span>
<span data-ttu-id="90c31-114">Domena AAD usługi OEM OEM usługi urządzeń z systemem Windows IoT</span><span class="sxs-lookup"><span data-stu-id="90c31-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="90c31-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="90c31-115">-BillingDomainName</span></span>
<span data-ttu-id="90c31-116">Domena AAD usługi urządzeń z systemem Windows IoT</span><span class="sxs-lookup"><span data-stu-id="90c31-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="90c31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c31-117">-DefaultProfile</span></span>
<span data-ttu-id="90c31-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="90c31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90c31-119">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="90c31-119">-Etag</span></span>
<span data-ttu-id="90c31-120">Pole Etag nie *jest* wymagane.</span><span class="sxs-lookup"><span data-stu-id="90c31-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="90c31-121">Jeśli wiadomość jest dostarczana w treści odpowiedzi, musi być również zapewniana jako nagłówek zgodnie z normalną konwencją tagów ETag.</span><span class="sxs-lookup"><span data-stu-id="90c31-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="90c31-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="90c31-122">-IfMatch</span></span>
<span data-ttu-id="90c31-123">Tag ETag usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="90c31-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="90c31-124">Nie należy określać tworzenia nowej usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="90c31-125">Wymagane do zaktualizowania istniejącej usługi urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="90c31-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="90c31-126">-Location</span></span>
<span data-ttu-id="90c31-127">Region platformy Azure, w którym znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="90c31-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="90c31-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="90c31-128">-Name</span></span>
<span data-ttu-id="90c31-129">Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="90c31-129">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c31-130">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="90c31-130">-Note</span></span>
<span data-ttu-id="90c31-131">Uwagi dotyczące usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="90c31-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="90c31-132">— Ilość</span><span class="sxs-lookup"><span data-stu-id="90c31-132">-Quantity</span></span>
<span data-ttu-id="90c31-133">Alokacja urządzeń w usłudze IoT systemu Windows</span><span class="sxs-lookup"><span data-stu-id="90c31-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="90c31-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c31-134">-ResourceGroupName</span></span>
<span data-ttu-id="90c31-135">Nazwa grupy zasobów zawierającej usługę urządzeń IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="90c31-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c31-136">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90c31-136">-SubscriptionId</span></span>
<span data-ttu-id="90c31-137">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="90c31-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c31-138">— Tag</span><span class="sxs-lookup"><span data-stu-id="90c31-138">-Tag</span></span>
<span data-ttu-id="90c31-139">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="90c31-139">Resource tags.</span></span>

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

### <span data-ttu-id="90c31-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90c31-140">-Confirm</span></span>
<span data-ttu-id="90c31-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90c31-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c31-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c31-142">-WhatIf</span></span>
<span data-ttu-id="90c31-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90c31-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c31-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="90c31-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c31-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c31-145">CommonParameters</span></span>
<span data-ttu-id="90c31-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c31-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c31-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90c31-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c31-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90c31-148">INPUTS</span></span>

## <span data-ttu-id="90c31-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90c31-149">OUTPUTS</span></span>

### <span data-ttu-id="90c31-150">Microsoft.Azure.PowerShell.Cmdlet.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="90c31-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="90c31-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="90c31-151">NOTES</span></span>

<span data-ttu-id="90c31-152">ALIASY</span><span class="sxs-lookup"><span data-stu-id="90c31-152">ALIASES</span></span>

## <span data-ttu-id="90c31-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90c31-153">RELATED LINKS</span></span>


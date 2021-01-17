---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491366"
---
# <span data-ttu-id="e4e0e-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="e4e0e-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="e4e0e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e0e-103">Tworzenie lub aktualizowanie metadanych usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="e4e0e-104">Typowym wzorcem do modyfikowania właściwości jest pobranie metadanych metadanych i zabezpieczeń usługi urządzenia IoT systemu Windows, a następnie połączenie ich z zmodyfikowanymi wartościami w nowej treści w celu zaktualizowania usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="e4e0e-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4e0e-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4e0e-106">Opis</span><span class="sxs-lookup"><span data-stu-id="e4e0e-106">DESCRIPTION</span></span>
<span data-ttu-id="e4e0e-107">Tworzenie lub aktualizowanie metadanych usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="e4e0e-108">Typowym wzorcem do modyfikowania właściwości jest pobranie metadanych metadanych i zabezpieczeń usługi urządzenia IoT systemu Windows, a następnie połączenie ich z zmodyfikowanymi wartościami w nowej treści w celu zaktualizowania usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="e4e0e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4e0e-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e0e-110">Przykład 1: tworzenie nowych usług IoT systemu Windows</span><span class="sxs-lookup"><span data-stu-id="e4e0e-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="e4e0e-111">To polecenie tworzy nowe usługi IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="e4e0e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4e0e-112">PARAMETERS</span></span>

### <span data-ttu-id="e4e0e-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="e4e0e-113">-AdminDomainName</span></span>
<span data-ttu-id="e4e0e-114">Domena usługi Windows IoT Device</span><span class="sxs-lookup"><span data-stu-id="e4e0e-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="e4e0e-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="e4e0e-115">-BillingDomainName</span></span>
<span data-ttu-id="e4e0e-116">Domena usługi ODM w usłudze urządzenia IoT z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="e4e0e-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="e4e0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e0e-117">-DefaultProfile</span></span>
<span data-ttu-id="e4e0e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4e0e-119">-ETag</span><span class="sxs-lookup"><span data-stu-id="e4e0e-119">-Etag</span></span>
<span data-ttu-id="e4e0e-120">Pole ETag *nie* jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="e4e0e-121">Jeśli jest podana w treści odpowiedzi, należy również podać jako nagłówek na zwykłych konwencjach ETag.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="e4e0e-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="e4e0e-122">-IfMatch</span></span>
<span data-ttu-id="e4e0e-123">Element ETag usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="e4e0e-124">Nie określaj możliwości tworzenia nowej usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="e4e0e-125">Wymagane do zaktualizowania istniejącej usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="e4e0e-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4e0e-126">-Location</span></span>
<span data-ttu-id="e4e0e-127">Obszar platformy Azure, w którym znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="e4e0e-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="e4e0e-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4e0e-128">-Name</span></span>
<span data-ttu-id="e4e0e-129">Nazwa usługi urządzeń z systemem Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="e4e0e-130">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="e4e0e-130">-Note</span></span>
<span data-ttu-id="e4e0e-131">Informacje o usłudze urządzeń IoT dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="e4e0e-132">-Ilość</span><span class="sxs-lookup"><span data-stu-id="e4e0e-132">-Quantity</span></span>
<span data-ttu-id="e4e0e-133">Przydziały urządzeń usługi urządzenia IoT z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="e4e0e-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="e4e0e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e0e-134">-ResourceGroupName</span></span>
<span data-ttu-id="e4e0e-135">Nazwa grupy zasobów zawierającej usługę urządzenia z usługami IoT systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="e4e0e-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e4e0e-136">-SubscriptionId</span></span>
<span data-ttu-id="e4e0e-137">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-137">The subscription identifier.</span></span>

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

### <span data-ttu-id="e4e0e-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4e0e-138">-Tag</span></span>
<span data-ttu-id="e4e0e-139">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-139">Resource tags.</span></span>

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

### <span data-ttu-id="e4e0e-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4e0e-140">-Confirm</span></span>
<span data-ttu-id="e4e0e-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e0e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e0e-142">-WhatIf</span></span>
<span data-ttu-id="e4e0e-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4e0e-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e0e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e0e-145">CommonParameters</span></span>
<span data-ttu-id="e4e0e-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e0e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e0e-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4e0e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e0e-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e0e-148">INPUTS</span></span>

## <span data-ttu-id="e4e0e-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4e0e-149">OUTPUTS</span></span>

### <span data-ttu-id="e4e0e-150">Microsoft. Azure. PowerShell. polecenia. WindowsIotServices. models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="e4e0e-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="e4e0e-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4e0e-151">NOTES</span></span>

<span data-ttu-id="e4e0e-152">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e4e0e-152">ALIASES</span></span>

## <span data-ttu-id="e4e0e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4e0e-153">RELATED LINKS</span></span>


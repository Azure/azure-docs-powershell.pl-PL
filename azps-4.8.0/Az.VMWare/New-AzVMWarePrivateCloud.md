---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222403"
---
# <span data-ttu-id="46e9e-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="46e9e-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="46e9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="46e9e-103">Tworzenie lub aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="46e9e-103">Create or update a private cloud</span></span>

## <span data-ttu-id="46e9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46e9e-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46e9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="46e9e-106">Tworzenie lub aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="46e9e-106">Create or update a private cloud</span></span>

## <span data-ttu-id="46e9e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46e9e-107">EXAMPLES</span></span>

### <span data-ttu-id="46e9e-108">Przykład 1: Tworzenie prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="46e9e-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="46e9e-109">Utwórz prywatną chmurę</span><span class="sxs-lookup"><span data-stu-id="46e9e-109">Create private cloud</span></span>

## <span data-ttu-id="46e9e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46e9e-110">PARAMETERS</span></span>

### <span data-ttu-id="46e9e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46e9e-111">-AsJob</span></span>
<span data-ttu-id="46e9e-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="46e9e-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e9e-113">-DefaultProfile</span></span>
<span data-ttu-id="46e9e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46e9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e9e-115">— Internet</span><span class="sxs-lookup"><span data-stu-id="46e9e-115">-Internet</span></span>
<span data-ttu-id="46e9e-116">Łączność z Internetem jest włączona lub wyłączona</span><span class="sxs-lookup"><span data-stu-id="46e9e-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="46e9e-117">-Location</span></span>
<span data-ttu-id="46e9e-118">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="46e9e-118">Resource location</span></span>

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

### <span data-ttu-id="46e9e-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="46e9e-119">-ManagementClusterSize</span></span>
<span data-ttu-id="46e9e-120">Rozmiar klastra</span><span class="sxs-lookup"><span data-stu-id="46e9e-120">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46e9e-121">-Name</span></span>
<span data-ttu-id="46e9e-122">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="46e9e-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="46e9e-123">-NetworkBlock</span></span>
<span data-ttu-id="46e9e-124">Blok adresów powinien być unikatowy w sieci wirtualnej w ramach abonamentu oraz lokalnego.</span><span class="sxs-lookup"><span data-stu-id="46e9e-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="46e9e-125">Upewnij się, że format CIDR jest zgodny z formatem (A. B. C. D/X), gdzie litery A, B, C, D należą do zakresu od 0 do 255, a wartość X należy do zakresu od 0 do 22</span><span class="sxs-lookup"><span data-stu-id="46e9e-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="46e9e-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="46e9e-126">-NoWait</span></span>
<span data-ttu-id="46e9e-127">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="46e9e-127">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="46e9e-128">-NsxtPassword</span></span>
<span data-ttu-id="46e9e-129">Opcjonalnie Ustaw hasło Menedżera NSX-T podczas tworzenia prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="46e9e-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="46e9e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e9e-130">-ResourceGroupName</span></span>
<span data-ttu-id="46e9e-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46e9e-131">The name of the resource group.</span></span>
<span data-ttu-id="46e9e-132">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="46e9e-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="46e9e-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="46e9e-133">-Sku</span></span>
<span data-ttu-id="46e9e-134">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="46e9e-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="46e9e-135">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="46e9e-135">-SubscriptionId</span></span>
<span data-ttu-id="46e9e-136">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="46e9e-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="46e9e-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="46e9e-137">-Tag</span></span>
<span data-ttu-id="46e9e-138">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="46e9e-138">Resource tags</span></span>

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

### <span data-ttu-id="46e9e-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="46e9e-139">-VcenterPassword</span></span>
<span data-ttu-id="46e9e-140">Opcjonalnie Ustaw hasło administratora vCenter podczas tworzenia prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="46e9e-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="46e9e-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46e9e-141">-Confirm</span></span>
<span data-ttu-id="46e9e-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46e9e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e9e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e9e-143">-WhatIf</span></span>
<span data-ttu-id="46e9e-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46e9e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e9e-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46e9e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e9e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e9e-146">CommonParameters</span></span>
<span data-ttu-id="46e9e-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e9e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e9e-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46e9e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e9e-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46e9e-149">INPUTS</span></span>

## <span data-ttu-id="46e9e-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46e9e-150">OUTPUTS</span></span>

### <span data-ttu-id="46e9e-151">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="46e9e-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="46e9e-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46e9e-152">NOTES</span></span>

<span data-ttu-id="46e9e-153">PISUJE</span><span class="sxs-lookup"><span data-stu-id="46e9e-153">ALIASES</span></span>

## <span data-ttu-id="46e9e-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46e9e-154">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.VMware/new-azVMwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 3e5e8fa4d098ce68899294a25866b4636c80878e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188730"
---
# <span data-ttu-id="883a8-101">New-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="883a8-101">New-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="883a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="883a8-102">SYNOPSIS</span></span>
<span data-ttu-id="883a8-103">Tworzenie lub aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="883a8-103">Create or update a private cloud</span></span>

## <span data-ttu-id="883a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="883a8-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="883a8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="883a8-105">DESCRIPTION</span></span>
<span data-ttu-id="883a8-106">Tworzenie lub aktualizowanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="883a8-106">Create or update a private cloud</span></span>

## <span data-ttu-id="883a8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="883a8-107">EXAMPLES</span></span>

### <span data-ttu-id="883a8-108">Przykład 1. Tworzenie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="883a8-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="883a8-109">Tworzenie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="883a8-109">Create private cloud</span></span>

## <span data-ttu-id="883a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="883a8-110">PARAMETERS</span></span>

### <span data-ttu-id="883a8-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="883a8-111">-AcceptEULA</span></span>
<span data-ttu-id="883a8-112">Zaakceptuj umowy EULA firmy AVS, pojawi się termin prawny bez podanego parametru</span><span class="sxs-lookup"><span data-stu-id="883a8-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="883a8-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="883a8-113">-AsJob</span></span>
<span data-ttu-id="883a8-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="883a8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="883a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883a8-115">-DefaultProfile</span></span>
<span data-ttu-id="883a8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="883a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="883a8-117">— Internet</span><span class="sxs-lookup"><span data-stu-id="883a8-117">-Internet</span></span>
<span data-ttu-id="883a8-118">Łączność z Internetem jest włączona lub wyłączona</span><span class="sxs-lookup"><span data-stu-id="883a8-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883a8-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="883a8-119">-Location</span></span>
<span data-ttu-id="883a8-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="883a8-120">Resource location</span></span>

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

### <span data-ttu-id="883a8-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="883a8-121">-ManagementClusterSize</span></span>
<span data-ttu-id="883a8-122">Rozmiar klastrów</span><span class="sxs-lookup"><span data-stu-id="883a8-122">The cluster size</span></span>

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

### <span data-ttu-id="883a8-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="883a8-123">-Name</span></span>
<span data-ttu-id="883a8-124">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="883a8-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="883a8-125">- NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="883a8-125">-NetworkBlock</span></span>
<span data-ttu-id="883a8-126">Blok adresów powinien być unikatowy w całej sieci VNet w subskrypcji, a także w środowisku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="883a8-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="883a8-127">Upewnij się, że format CIDR jest zgodny z (A.B.C.D/X), gdzie A,B,C,D należy między 0 a 255, a X między 0 a 22</span><span class="sxs-lookup"><span data-stu-id="883a8-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="883a8-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="883a8-128">-NoWait</span></span>
<span data-ttu-id="883a8-129">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="883a8-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="883a8-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="883a8-130">-NsxtPassword</span></span>
<span data-ttu-id="883a8-131">Opcjonalnie możesz ustawić hasło menedżera NSX-T podczas tworzenia chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="883a8-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="883a8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883a8-132">-ResourceGroupName</span></span>
<span data-ttu-id="883a8-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="883a8-133">The name of the resource group.</span></span>
<span data-ttu-id="883a8-134">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="883a8-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="883a8-135">- SKU</span><span class="sxs-lookup"><span data-stu-id="883a8-135">-Sku</span></span>
<span data-ttu-id="883a8-136">Nazwa sku.</span><span class="sxs-lookup"><span data-stu-id="883a8-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="883a8-137">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="883a8-137">-SubscriptionId</span></span>
<span data-ttu-id="883a8-138">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="883a8-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="883a8-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="883a8-139">-Tag</span></span>
<span data-ttu-id="883a8-140">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="883a8-140">Resource tags</span></span>

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

### <span data-ttu-id="883a8-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="883a8-141">-VcenterPassword</span></span>
<span data-ttu-id="883a8-142">Opcjonalnie możesz ustawić hasło administratora vCenter podczas tworzenia chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="883a8-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="883a8-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="883a8-143">-Confirm</span></span>
<span data-ttu-id="883a8-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="883a8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883a8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883a8-145">-WhatIf</span></span>
<span data-ttu-id="883a8-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="883a8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="883a8-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="883a8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883a8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883a8-148">CommonParameters</span></span>
<span data-ttu-id="883a8-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="883a8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883a8-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="883a8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883a8-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="883a8-151">INPUTS</span></span>

## <span data-ttu-id="883a8-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="883a8-152">OUTPUTS</span></span>

### <span data-ttu-id="883a8-153">Microsoft.Azure.PowerShell.cmdlet.vLogne.models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="883a8-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="883a8-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="883a8-154">NOTES</span></span>

<span data-ttu-id="883a8-155">ALIASY</span><span class="sxs-lookup"><span data-stu-id="883a8-155">ALIASES</span></span>

## <span data-ttu-id="883a8-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="883a8-156">RELATED LINKS</span></span>


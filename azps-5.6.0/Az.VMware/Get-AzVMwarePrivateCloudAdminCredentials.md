---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 88ecb5baff31ddcc27ce090f19a868c4d393c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987169"
---
# <span data-ttu-id="098f0-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="098f0-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="098f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098f0-102">SYNOPSIS</span></span>
<span data-ttu-id="098f0-103">Lista poświadczeń administratora dla chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="098f0-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="098f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="098f0-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="098f0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="098f0-105">DESCRIPTION</span></span>
<span data-ttu-id="098f0-106">Lista poświadczeń administratora dla chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="098f0-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="098f0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="098f0-107">EXAMPLES</span></span>

### <span data-ttu-id="098f0-108">Przykład 1. Uzyskiwanie poświadczeń administratora chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="098f0-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="098f0-109">Uzyskiwanie poświadczeń administratora chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="098f0-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="098f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="098f0-110">PARAMETERS</span></span>

### <span data-ttu-id="098f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098f0-111">-DefaultProfile</span></span>
<span data-ttu-id="098f0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="098f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="098f0-113">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="098f0-113">-PrivateCloudName</span></span>
<span data-ttu-id="098f0-114">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="098f0-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="098f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="098f0-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="098f0-116">The name of the resource group.</span></span>
<span data-ttu-id="098f0-117">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="098f0-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="098f0-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="098f0-118">-SubscriptionId</span></span>
<span data-ttu-id="098f0-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="098f0-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="098f0-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="098f0-120">-Confirm</span></span>
<span data-ttu-id="098f0-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="098f0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098f0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098f0-122">-WhatIf</span></span>
<span data-ttu-id="098f0-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="098f0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="098f0-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="098f0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098f0-125">CommonParameters</span></span>
<span data-ttu-id="098f0-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="098f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098f0-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="098f0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098f0-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="098f0-128">INPUTS</span></span>

## <span data-ttu-id="098f0-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="098f0-129">OUTPUTS</span></span>

### <span data-ttu-id="098f0-130">Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="098f0-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="098f0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="098f0-131">NOTES</span></span>

<span data-ttu-id="098f0-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="098f0-132">ALIASES</span></span>

## <span data-ttu-id="098f0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="098f0-133">RELATED LINKS</span></span>


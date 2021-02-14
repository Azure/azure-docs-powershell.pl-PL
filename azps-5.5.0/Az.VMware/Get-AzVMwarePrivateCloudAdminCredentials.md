---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 7502bbd96371aa505d8d927dfb9a491c2ca32b34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241579"
---
# <span data-ttu-id="0f006-101">Get-AzVMwarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="0f006-101">Get-AzVMwarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="0f006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f006-102">SYNOPSIS</span></span>
<span data-ttu-id="0f006-103">Lista poświadczeń administratora dla chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f006-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="0f006-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f006-104">SYNTAX</span></span>

```
Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f006-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f006-105">DESCRIPTION</span></span>
<span data-ttu-id="0f006-106">Lista poświadczeń administratora dla chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f006-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="0f006-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f006-107">EXAMPLES</span></span>

### <span data-ttu-id="0f006-108">Przykład 1. Uzyskiwanie poświadczeń administratora chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f006-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="0f006-109">Uzyskiwanie poświadczeń administratora chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f006-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="0f006-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f006-110">PARAMETERS</span></span>

### <span data-ttu-id="0f006-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f006-111">-DefaultProfile</span></span>
<span data-ttu-id="0f006-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f006-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f006-113">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0f006-113">-PrivateCloudName</span></span>
<span data-ttu-id="0f006-114">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f006-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="0f006-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f006-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f006-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f006-116">The name of the resource group.</span></span>
<span data-ttu-id="0f006-117">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0f006-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0f006-118">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f006-118">-SubscriptionId</span></span>
<span data-ttu-id="0f006-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0f006-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0f006-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f006-120">-Confirm</span></span>
<span data-ttu-id="0f006-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f006-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f006-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f006-122">-WhatIf</span></span>
<span data-ttu-id="0f006-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f006-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f006-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0f006-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f006-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f006-125">CommonParameters</span></span>
<span data-ttu-id="0f006-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f006-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f006-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f006-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f006-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f006-128">INPUTS</span></span>

## <span data-ttu-id="0f006-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f006-129">OUTPUTS</span></span>

### <span data-ttu-id="0f006-130">Microsoft.Azure.PowerShell.Cmdlet.V Jak.Model.Api200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="0f006-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="0f006-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f006-131">NOTES</span></span>

<span data-ttu-id="0f006-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0f006-132">ALIASES</span></span>

## <span data-ttu-id="0f006-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f006-133">RELATED LINKS</span></span>


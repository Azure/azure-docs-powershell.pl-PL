---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063786"
---
# <span data-ttu-id="10d7b-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="10d7b-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="10d7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="10d7b-103">Wyświetlanie listy poświadczeń administratora chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="10d7b-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="10d7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10d7b-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10d7b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="10d7b-106">Wyświetlanie listy poświadczeń administratora chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="10d7b-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="10d7b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="10d7b-108">Przykład 1: Uzyskaj poświadczenia administratora chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="10d7b-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="10d7b-109">Uzyskiwanie poświadczenia administratora prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="10d7b-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="10d7b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10d7b-110">PARAMETERS</span></span>

### <span data-ttu-id="10d7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d7b-111">-DefaultProfile</span></span>
<span data-ttu-id="10d7b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10d7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10d7b-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="10d7b-113">-PrivateCloudName</span></span>
<span data-ttu-id="10d7b-114">Nazwa prywatnej chmury</span><span class="sxs-lookup"><span data-stu-id="10d7b-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="10d7b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d7b-115">-ResourceGroupName</span></span>
<span data-ttu-id="10d7b-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10d7b-116">The name of the resource group.</span></span>
<span data-ttu-id="10d7b-117">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="10d7b-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="10d7b-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="10d7b-118">-SubscriptionId</span></span>
<span data-ttu-id="10d7b-119">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="10d7b-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="10d7b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10d7b-120">-Confirm</span></span>
<span data-ttu-id="10d7b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10d7b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d7b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d7b-122">-WhatIf</span></span>
<span data-ttu-id="10d7b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10d7b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d7b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10d7b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d7b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d7b-125">CommonParameters</span></span>
<span data-ttu-id="10d7b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d7b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d7b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10d7b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d7b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10d7b-128">INPUTS</span></span>

## <span data-ttu-id="10d7b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10d7b-129">OUTPUTS</span></span>

### <span data-ttu-id="10d7b-130">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="10d7b-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="10d7b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10d7b-131">NOTES</span></span>

<span data-ttu-id="10d7b-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="10d7b-132">ALIASES</span></span>

## <span data-ttu-id="10d7b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10d7b-133">RELATED LINKS</span></span>


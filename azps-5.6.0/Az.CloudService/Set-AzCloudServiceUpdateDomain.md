---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4b47992eb290c0a34ac2b368017d443051a6bb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988450"
---
# <span data-ttu-id="f78ab-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="f78ab-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="f78ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f78ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f78ab-103">Aktualizuje wystąpienia ról w określonej domenie aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="f78ab-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="f78ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f78ab-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f78ab-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f78ab-105">DESCRIPTION</span></span>
<span data-ttu-id="f78ab-106">Aktualizuje wystąpienia ról w określonej domenie aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="f78ab-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="f78ab-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f78ab-107">EXAMPLES</span></span>

### <span data-ttu-id="f78ab-108">Przykład 1. Aktualizowanie wystąpienia roli w domenie aktualizacji</span><span class="sxs-lookup"><span data-stu-id="f78ab-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="f78ab-109">To polecenie aktualizuje wystąpienia ról w domenie aktualizacji 0 usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="f78ab-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="f78ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f78ab-110">PARAMETERS</span></span>

### <span data-ttu-id="f78ab-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f78ab-111">-AsJob</span></span>
<span data-ttu-id="f78ab-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f78ab-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f78ab-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f78ab-113">-CloudServiceName</span></span>
<span data-ttu-id="f78ab-114">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="f78ab-114">Name of the cloud service.</span></span>

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

### <span data-ttu-id="f78ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78ab-115">-DefaultProfile</span></span>
<span data-ttu-id="f78ab-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f78ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f78ab-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f78ab-117">-NoWait</span></span>
<span data-ttu-id="f78ab-118">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f78ab-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f78ab-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f78ab-119">-PassThru</span></span>
<span data-ttu-id="f78ab-120">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="f78ab-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f78ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f78ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="f78ab-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f78ab-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="f78ab-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f78ab-123">-SubscriptionId</span></span>
<span data-ttu-id="f78ab-124">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f78ab-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f78ab-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="f78ab-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f78ab-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="f78ab-126">-UpdateDomain</span></span>
<span data-ttu-id="f78ab-127">Określa wartość całkowitą identyfikującą domenę aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="f78ab-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="f78ab-128">Domeny aktualizacji są identyfikowane za pomocą indeksu opartego na zeru: pierwsza domena aktualizacji ma identyfikator 0, druga ma identyfikator 1 i tak dalej.</span><span class="sxs-lookup"><span data-stu-id="f78ab-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

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

### <span data-ttu-id="f78ab-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f78ab-129">-Confirm</span></span>
<span data-ttu-id="f78ab-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f78ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f78ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f78ab-131">-WhatIf</span></span>
<span data-ttu-id="f78ab-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78ab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f78ab-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f78ab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f78ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78ab-134">CommonParameters</span></span>
<span data-ttu-id="f78ab-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78ab-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f78ab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78ab-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f78ab-137">INPUTS</span></span>

## <span data-ttu-id="f78ab-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f78ab-138">OUTPUTS</span></span>

### <span data-ttu-id="f78ab-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f78ab-139">System.Boolean</span></span>

## <span data-ttu-id="f78ab-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f78ab-140">NOTES</span></span>

<span data-ttu-id="f78ab-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f78ab-141">ALIASES</span></span>

## <span data-ttu-id="f78ab-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f78ab-142">RELATED LINKS</span></span>


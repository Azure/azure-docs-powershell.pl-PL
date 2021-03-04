---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 503d20a8473c83a9b2ca7ca1ec19deab6db7103c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953601"
---
# <span data-ttu-id="20f0f-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="20f0f-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="20f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="20f0f-103">Przywracanie elastycznego serwera PostgreSQL z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="20f0f-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="20f0f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="20f0f-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20f0f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="20f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="20f0f-106">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="20f0f-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="20f0f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="20f0f-107">EXAMPLES</span></span>

### <span data-ttu-id="20f0f-108">Przykład 1. Przywracanie serwera PostgreSql przy użyciu funkcji Przywracania punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="20f0f-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="20f0f-109">Te polecenia cmdlet przywrócą serwer PostgreSql przy użyciu funkcji przywracania pointintime.</span><span class="sxs-lookup"><span data-stu-id="20f0f-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="20f0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20f0f-110">PARAMETERS</span></span>

### <span data-ttu-id="20f0f-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="20f0f-111">-AsJob</span></span>
<span data-ttu-id="20f0f-112">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="20f0f-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="20f0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f0f-113">-DefaultProfile</span></span>
<span data-ttu-id="20f0f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="20f0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20f0f-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="20f0f-115">-Location</span></span>
<span data-ttu-id="20f0f-116">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="20f0f-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="20f0f-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="20f0f-117">-Name</span></span>
<span data-ttu-id="20f0f-118">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="20f0f-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f0f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="20f0f-119">-NoWait</span></span>
<span data-ttu-id="20f0f-120">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="20f0f-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="20f0f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f0f-121">-ResourceGroupName</span></span>
<span data-ttu-id="20f0f-122">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="20f0f-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="20f0f-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="20f0f-123">-RestorePointInTime</span></span>
<span data-ttu-id="20f0f-124">Czas na przywrócenie z (format ISO8601), na przykład 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="20f0f-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f0f-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="20f0f-125">-SourceServerName</span></span>
<span data-ttu-id="20f0f-126">Nazwa serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="20f0f-126">The name of the source server.</span></span>

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

### <span data-ttu-id="20f0f-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20f0f-127">-SubscriptionId</span></span>
<span data-ttu-id="20f0f-128">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="20f0f-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="20f0f-129">— Strefa</span><span class="sxs-lookup"><span data-stu-id="20f0f-129">-Zone</span></span>
<span data-ttu-id="20f0f-130">Strefa dostępności do obsługi administracyjnej zasobu.</span><span class="sxs-lookup"><span data-stu-id="20f0f-130">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="20f0f-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20f0f-131">-Confirm</span></span>
<span data-ttu-id="20f0f-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="20f0f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f0f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f0f-133">-WhatIf</span></span>
<span data-ttu-id="20f0f-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20f0f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20f0f-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="20f0f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f0f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f0f-136">CommonParameters</span></span>
<span data-ttu-id="20f0f-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f0f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f0f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20f0f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f0f-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20f0f-139">INPUTS</span></span>

## <span data-ttu-id="20f0f-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20f0f-140">OUTPUTS</span></span>

### <span data-ttu-id="20f0f-141">Microsoft.Azure.PowerShell.cmdlet.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="20f0f-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="20f0f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="20f0f-142">NOTES</span></span>

<span data-ttu-id="20f0f-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="20f0f-143">ALIASES</span></span>

## <span data-ttu-id="20f0f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20f0f-144">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: e8554f0ac88cf3d69e36282b7e310cc92b41d6db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179083"
---
# <span data-ttu-id="f1550-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="f1550-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="f1550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1550-102">SYNOPSIS</span></span>
<span data-ttu-id="f1550-103">Przywracanie elastycznego serwera PostgreSQL z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f1550-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="f1550-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1550-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1550-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1550-105">DESCRIPTION</span></span>
<span data-ttu-id="f1550-106">Przywracanie serwera z istniejącej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f1550-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="f1550-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1550-107">EXAMPLES</span></span>

### <span data-ttu-id="f1550-108">Przykład 1. Przywracanie serwera PostgreSql przy użyciu funkcji Przywracania punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="f1550-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="f1550-109">Te polecenia cmdlet przywróć serwer PostgreSql przy użyciu funkcji przywracania PointInTime.</span><span class="sxs-lookup"><span data-stu-id="f1550-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="f1550-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1550-110">PARAMETERS</span></span>

### <span data-ttu-id="f1550-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f1550-111">-AsJob</span></span>
<span data-ttu-id="f1550-112">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="f1550-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="f1550-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1550-113">-DefaultProfile</span></span>
<span data-ttu-id="f1550-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1550-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1550-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f1550-115">-Location</span></span>
<span data-ttu-id="f1550-116">Lokalizacja, w którym znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="f1550-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f1550-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1550-117">-Name</span></span>
<span data-ttu-id="f1550-118">Nazwa serwera.</span><span class="sxs-lookup"><span data-stu-id="f1550-118">The name of the server.</span></span>

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

### <span data-ttu-id="f1550-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1550-119">-NoWait</span></span>
<span data-ttu-id="f1550-120">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="f1550-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="f1550-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1550-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1550-122">Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="f1550-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f1550-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="f1550-123">-RestorePointInTime</span></span>
<span data-ttu-id="f1550-124">Czas na przywrócenie z (format ISO8601), na przykład 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="f1550-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

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

### <span data-ttu-id="f1550-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="f1550-125">-SourceServerName</span></span>
<span data-ttu-id="f1550-126">Nazwa serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="f1550-126">The name of the source server.</span></span>

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

### <span data-ttu-id="f1550-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1550-127">-SubscriptionId</span></span>
<span data-ttu-id="f1550-128">Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f1550-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f1550-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1550-129">-Confirm</span></span>
<span data-ttu-id="f1550-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f1550-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1550-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1550-131">-WhatIf</span></span>
<span data-ttu-id="f1550-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1550-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1550-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f1550-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1550-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1550-134">CommonParameters</span></span>
<span data-ttu-id="f1550-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1550-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1550-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1550-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1550-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1550-137">INPUTS</span></span>

## <span data-ttu-id="f1550-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1550-138">OUTPUTS</span></span>

### <span data-ttu-id="f1550-139">Microsoft.Azure.PowerShell.Cmdlet.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="f1550-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="f1550-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1550-140">NOTES</span></span>

<span data-ttu-id="f1550-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f1550-141">ALIASES</span></span>

## <span data-ttu-id="f1550-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1550-142">RELATED LINKS</span></span>


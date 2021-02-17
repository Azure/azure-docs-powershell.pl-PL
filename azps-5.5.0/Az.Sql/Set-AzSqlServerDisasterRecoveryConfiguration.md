---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187970"
---
# <span data-ttu-id="55917-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55917-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="55917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55917-102">SYNOPSIS</span></span>
<span data-ttu-id="55917-103">Modyfikuje konfigurację odzyskiwania serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="55917-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="55917-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55917-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55917-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="55917-105">DESCRIPTION</span></span>
<span data-ttu-id="55917-106">Polecenie **cmdlet Set-AzSqlServerDisasterRecoveryConfiguration** modyfikuje konfigurację odzyskiwania serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="55917-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="55917-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55917-107">EXAMPLES</span></span>

## <span data-ttu-id="55917-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55917-108">PARAMETERS</span></span>

### <span data-ttu-id="55917-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="55917-109">-AllowDataLoss</span></span>
<span data-ttu-id="55917-110">Wskazuje, że operacja trybu failover zezwala na utratę danych.</span><span class="sxs-lookup"><span data-stu-id="55917-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="55917-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="55917-111">-AsJob</span></span>
<span data-ttu-id="55917-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="55917-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55917-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55917-113">-DefaultProfile</span></span>
<span data-ttu-id="55917-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="55917-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55917-115">- Failover</span><span class="sxs-lookup"><span data-stu-id="55917-115">-Failover</span></span>
<span data-ttu-id="55917-116">Oznacza, że ta operacja jest trybem failover.</span><span class="sxs-lookup"><span data-stu-id="55917-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55917-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55917-117">-ResourceGroupName</span></span>
<span data-ttu-id="55917-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55917-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55917-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55917-119">-ServerName</span></span>
<span data-ttu-id="55917-120">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="55917-120">Specifies the name of a SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55917-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="55917-121">-VirtualEndpointName</span></span>
<span data-ttu-id="55917-122">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="55917-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="55917-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55917-123">-Confirm</span></span>
<span data-ttu-id="55917-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="55917-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55917-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55917-125">-WhatIf</span></span>
<span data-ttu-id="55917-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55917-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55917-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="55917-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55917-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55917-128">CommonParameters</span></span>
<span data-ttu-id="55917-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55917-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55917-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55917-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55917-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55917-131">INPUTS</span></span>

### <span data-ttu-id="55917-132">System.String</span><span class="sxs-lookup"><span data-stu-id="55917-132">System.String</span></span>

## <span data-ttu-id="55917-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55917-133">OUTPUTS</span></span>

### <span data-ttu-id="55917-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="55917-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="55917-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55917-135">NOTES</span></span>

## <span data-ttu-id="55917-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55917-136">RELATED LINKS</span></span>

[<span data-ttu-id="55917-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55917-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="55917-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55917-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="55917-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55917-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="55917-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="55917-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

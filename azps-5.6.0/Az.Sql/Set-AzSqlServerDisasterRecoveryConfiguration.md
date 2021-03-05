---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a1f91c01d3183551cbabf58754fbe628e1feea32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992391"
---
# <span data-ttu-id="064a0-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="064a0-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="064a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="064a0-102">SYNOPSIS</span></span>
<span data-ttu-id="064a0-103">Modyfikuje konfigurację odzyskiwania serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="064a0-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="064a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="064a0-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="064a0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="064a0-105">DESCRIPTION</span></span>
<span data-ttu-id="064a0-106">Polecenie **cmdlet Set-AzSqlServerDisasterRecoveryConfiguration** modyfikuje konfigurację odzyskiwania serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="064a0-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="064a0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="064a0-107">EXAMPLES</span></span>

## <span data-ttu-id="064a0-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="064a0-108">PARAMETERS</span></span>

### <span data-ttu-id="064a0-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="064a0-109">-AllowDataLoss</span></span>
<span data-ttu-id="064a0-110">Wskazuje, że operacja trybu failover zezwala na utratę danych.</span><span class="sxs-lookup"><span data-stu-id="064a0-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="064a0-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="064a0-111">-AsJob</span></span>
<span data-ttu-id="064a0-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="064a0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="064a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064a0-113">-DefaultProfile</span></span>
<span data-ttu-id="064a0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="064a0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="064a0-115">- Failover</span><span class="sxs-lookup"><span data-stu-id="064a0-115">-Failover</span></span>
<span data-ttu-id="064a0-116">Oznacza, że ta operacja jest trybem failover.</span><span class="sxs-lookup"><span data-stu-id="064a0-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="064a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064a0-117">-ResourceGroupName</span></span>
<span data-ttu-id="064a0-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="064a0-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="064a0-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="064a0-119">-ServerName</span></span>
<span data-ttu-id="064a0-120">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="064a0-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="064a0-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="064a0-121">-VirtualEndpointName</span></span>
<span data-ttu-id="064a0-122">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="064a0-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="064a0-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="064a0-123">-Confirm</span></span>
<span data-ttu-id="064a0-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="064a0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="064a0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="064a0-125">-WhatIf</span></span>
<span data-ttu-id="064a0-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="064a0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="064a0-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="064a0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="064a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064a0-128">CommonParameters</span></span>
<span data-ttu-id="064a0-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064a0-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="064a0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064a0-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="064a0-131">INPUTS</span></span>

### <span data-ttu-id="064a0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="064a0-132">System.String</span></span>

## <span data-ttu-id="064a0-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="064a0-133">OUTPUTS</span></span>

### <span data-ttu-id="064a0-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="064a0-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="064a0-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="064a0-135">NOTES</span></span>

## <span data-ttu-id="064a0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="064a0-136">RELATED LINKS</span></span>

[<span data-ttu-id="064a0-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="064a0-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="064a0-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="064a0-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="064a0-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="064a0-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="064a0-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="064a0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

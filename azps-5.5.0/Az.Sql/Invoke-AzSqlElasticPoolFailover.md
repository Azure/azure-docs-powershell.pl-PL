---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176899"
---
# <span data-ttu-id="46f13-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="46f13-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="46f13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f13-102">SYNOPSIS</span></span>
<span data-ttu-id="46f13-103">W przypadku trybu failover jest elastyczna pula.</span><span class="sxs-lookup"><span data-stu-id="46f13-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="46f13-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46f13-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46f13-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="46f13-105">DESCRIPTION</span></span>
<span data-ttu-id="46f13-106">Polecenie Invoke-AzSqlElasticPoolFailover trybu failovers elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="46f13-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="46f13-107">Po uruchomieniu tego polecenia cmdlet trybu failover wystąpi we wszystkich bazach danych w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="46f13-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="46f13-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46f13-108">EXAMPLES</span></span>

### <span data-ttu-id="46f13-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46f13-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="46f13-110">To polecenie przejmie w stanie failover elastyczną pulę o nazwie "Pool01" na serwerze o nazwie "Server01".</span><span class="sxs-lookup"><span data-stu-id="46f13-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="46f13-111">Oznacza to, że trybu failover wystąpi we wszystkich bazach danych w puli elastycznej o nazwie "Pool01".</span><span class="sxs-lookup"><span data-stu-id="46f13-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="46f13-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46f13-112">PARAMETERS</span></span>

### <span data-ttu-id="46f13-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="46f13-113">-AsJob</span></span>
<span data-ttu-id="46f13-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="46f13-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46f13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f13-115">-DefaultProfile</span></span>
<span data-ttu-id="46f13-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46f13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f13-117">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="46f13-117">-ElasticPoolName</span></span>
<span data-ttu-id="46f13-118">Nazwa puli elastycznej sql azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="46f13-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f13-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="46f13-119">-Force</span></span>
<span data-ttu-id="46f13-120">Pomiń komunikat z potwierdzeniem wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="46f13-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="46f13-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46f13-121">-PassThru</span></span>
<span data-ttu-id="46f13-122">Po pomyślnym wykonaniu zwraca wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="46f13-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="46f13-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="46f13-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46f13-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f13-124">-ResourceGroupName</span></span>
<span data-ttu-id="46f13-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46f13-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="46f13-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="46f13-126">-ServerName</span></span>
<span data-ttu-id="46f13-127">Nazwa serwera Azure SQL Server, w którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="46f13-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="46f13-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46f13-128">-Confirm</span></span>
<span data-ttu-id="46f13-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46f13-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f13-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f13-130">-WhatIf</span></span>
<span data-ttu-id="46f13-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46f13-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46f13-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="46f13-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f13-133">CommonParameters</span></span>
<span data-ttu-id="46f13-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f13-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46f13-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f13-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46f13-136">INPUTS</span></span>

### <span data-ttu-id="46f13-137">System.String</span><span class="sxs-lookup"><span data-stu-id="46f13-137">System.String</span></span>

## <span data-ttu-id="46f13-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46f13-138">OUTPUTS</span></span>

## <span data-ttu-id="46f13-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46f13-139">NOTES</span></span>

## <span data-ttu-id="46f13-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46f13-140">RELATED LINKS</span></span>

[<span data-ttu-id="46f13-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46f13-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="46f13-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="46f13-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="46f13-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="46f13-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="46f13-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="46f13-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="46f13-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46f13-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="46f13-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46f13-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="46f13-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="46f13-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="46f13-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="46f13-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178355"
---
# <span data-ttu-id="1398a-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1398a-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="1398a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1398a-102">SYNOPSIS</span></span>
<span data-ttu-id="1398a-103">Przełącza pomocniczą bazę danych jako podstawową w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="1398a-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="1398a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1398a-104">SYNTAX</span></span>

### <span data-ttu-id="1398a-105">NoOptionsSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1398a-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1398a-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="1398a-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1398a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1398a-107">DESCRIPTION</span></span>
<span data-ttu-id="1398a-108">Polecenie **cmdlet Set-AzSqlDatabaseSecondary** przełącza pomocniczą bazę danych jako podstawową w celu zainicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="1398a-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="1398a-109">To polecenie cmdlet jest zaprojektowane jako ogólne polecenie konfiguracji, ale obecnie jest ograniczone do inicjowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="1398a-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="1398a-110">Określ parametr *AllowDataLoss,* aby zainicjować wymuszanie trybu failover podczas awarii.</span><span class="sxs-lookup"><span data-stu-id="1398a-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="1398a-111">Nie musisz określać tego parametru podczas wykonywania planowanej operacji, takiej jak przechodzenie do szczegółów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1398a-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="1398a-112">W drugim przypadku pomocnicza baza danych jest synchronizowana z podstawową bazą danych przed jej przełączeniem.</span><span class="sxs-lookup"><span data-stu-id="1398a-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="1398a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1398a-113">EXAMPLES</span></span>

### <span data-ttu-id="1398a-114">Przykład 1. Inicjowanie planowanej trybu failover</span><span class="sxs-lookup"><span data-stu-id="1398a-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="1398a-115">Przykład 2. Zainicjowanie wymuszonego trybu failover (z potencjalną utratą danych)</span><span class="sxs-lookup"><span data-stu-id="1398a-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="1398a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1398a-116">PARAMETERS</span></span>

### <span data-ttu-id="1398a-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="1398a-117">-AllowDataLoss</span></span>
<span data-ttu-id="1398a-118">Wskazuje, że ta operacja trybu failover zezwala na utratę danych.</span><span class="sxs-lookup"><span data-stu-id="1398a-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1398a-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1398a-119">-AsJob</span></span>
<span data-ttu-id="1398a-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1398a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1398a-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1398a-121">-DatabaseName</span></span>
<span data-ttu-id="1398a-122">Określa nazwę pomocniczej bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1398a-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1398a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1398a-123">-DefaultProfile</span></span>
<span data-ttu-id="1398a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1398a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1398a-125">- Failover</span><span class="sxs-lookup"><span data-stu-id="1398a-125">-Failover</span></span>
<span data-ttu-id="1398a-126">Oznacza, że ta operacja jest trybem failover.</span><span class="sxs-lookup"><span data-stu-id="1398a-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1398a-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1398a-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1398a-128">Określa nazwę grupy zasobów, do której jest przypisana partnerska baza danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1398a-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1398a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1398a-129">-ResourceGroupName</span></span>
<span data-ttu-id="1398a-130">Określa nazwę grupy zasobów, do której jest przypisana usługa Azure SQL Database Secondary.</span><span class="sxs-lookup"><span data-stu-id="1398a-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="1398a-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1398a-131">-ServerName</span></span>
<span data-ttu-id="1398a-132">Określa nazwę serwera SQL hostowego pomocniczego bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1398a-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="1398a-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1398a-133">-Confirm</span></span>
<span data-ttu-id="1398a-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1398a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1398a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1398a-135">-WhatIf</span></span>
<span data-ttu-id="1398a-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1398a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1398a-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1398a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1398a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1398a-138">CommonParameters</span></span>
<span data-ttu-id="1398a-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1398a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1398a-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1398a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1398a-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1398a-141">INPUTS</span></span>

### <span data-ttu-id="1398a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1398a-142">System.String</span></span>

## <span data-ttu-id="1398a-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1398a-143">OUTPUTS</span></span>

### <span data-ttu-id="1398a-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1398a-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="1398a-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1398a-145">NOTES</span></span>

## <span data-ttu-id="1398a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1398a-146">RELATED LINKS</span></span>

[<span data-ttu-id="1398a-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1398a-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="1398a-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1398a-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="1398a-149">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1398a-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

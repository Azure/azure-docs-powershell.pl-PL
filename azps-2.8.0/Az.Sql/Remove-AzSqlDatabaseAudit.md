---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: ad0103e2a4d529a4f306749a1d55ca0b6eadc013
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887353"
---
# <span data-ttu-id="d0ff6-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d0ff6-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="d0ff6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ff6-103">Usuwa ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="d0ff6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0ff6-104">SYNTAX</span></span>

### <span data-ttu-id="d0ff6-105">DatabaseParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0ff6-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0ff6-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0ff6-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0ff6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0ff6-107">DESCRIPTION</span></span>
<span data-ttu-id="d0ff6-108">Polecenie cmdlet **Remove-AzSqlDatabaseAudit** usuwa ustawienia inspekcji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="d0ff6-109">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="d0ff6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0ff6-110">EXAMPLES</span></span>

### <span data-ttu-id="d0ff6-111">Przykład 1: usuwanie ustawień inspekcji bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d0ff6-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="d0ff6-112">Przykład 2: usuwanie za pośrednictwem rurociągu ustawień inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="d0ff6-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="d0ff6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0ff6-113">PARAMETERS</span></span>

### <span data-ttu-id="d0ff6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0ff6-114">-DatabaseName</span></span>
<span data-ttu-id="d0ff6-115">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0ff6-116">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="d0ff6-116">-DatabaseObject</span></span>
<span data-ttu-id="d0ff6-117">Obiekt bazy danych do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0ff6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ff6-118">-DefaultProfile</span></span>
<span data-ttu-id="d0ff6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ff6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ff6-120">-ResourceGroupName</span></span>
<span data-ttu-id="d0ff6-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0ff6-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d0ff6-122">-ServerName</span></span>
<span data-ttu-id="d0ff6-123">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0ff6-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0ff6-124">-Confirm</span></span>
<span data-ttu-id="d0ff6-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0ff6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0ff6-126">-WhatIf</span></span>
<span data-ttu-id="d0ff6-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0ff6-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0ff6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ff6-129">CommonParameters</span></span>
<span data-ttu-id="d0ff6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ff6-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0ff6-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ff6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0ff6-132">INPUTS</span></span>

### <span data-ttu-id="d0ff6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d0ff6-133">System.String</span></span>

### <span data-ttu-id="d0ff6-134">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d0ff6-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d0ff6-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0ff6-135">OUTPUTS</span></span>

### <span data-ttu-id="d0ff6-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0ff6-136">System.Boolean</span></span>

## <span data-ttu-id="d0ff6-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0ff6-137">NOTES</span></span>

## <span data-ttu-id="d0ff6-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0ff6-138">RELATED LINKS</span></span>

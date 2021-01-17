---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353662"
---
# <span data-ttu-id="34e1e-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="34e1e-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="34e1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="34e1e-103">Usuwa dany punkt przywracania z bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="34e1e-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="34e1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34e1e-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="34e1e-106">Polecenie cmdlet **Remove-AzSqlDatabaseRestorePoint** usuwa dany punkt przywracania z bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="34e1e-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="34e1e-107">To polecenie cmdlet jest obecnie obsługiwane przez usługę hurtowni danych programu SQL Server w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="34e1e-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="34e1e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34e1e-108">EXAMPLES</span></span>

### <span data-ttu-id="34e1e-109">Przykład 1. usuwa punkt przywracania</span><span class="sxs-lookup"><span data-stu-id="34e1e-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="34e1e-110">To polecenie usuwa punkt przywracania bazy danych SQL Azure o danej dacie utworzenia.</span><span class="sxs-lookup"><span data-stu-id="34e1e-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="34e1e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34e1e-111">PARAMETERS</span></span>

### <span data-ttu-id="34e1e-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34e1e-112">-DatabaseName</span></span>
<span data-ttu-id="34e1e-113">Określa nazwę bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="34e1e-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="34e1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e1e-114">-DefaultProfile</span></span>
<span data-ttu-id="34e1e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="34e1e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34e1e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34e1e-116">-PassThru</span></span>
<span data-ttu-id="34e1e-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="34e1e-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34e1e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e1e-118">-ResourceGroupName</span></span>
<span data-ttu-id="34e1e-119">Określa nazwę grupy zasobów, do której jest przypisana baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="34e1e-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="34e1e-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="34e1e-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="34e1e-121">Określa datę utworzenia punktu przywracania.</span><span class="sxs-lookup"><span data-stu-id="34e1e-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e1e-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="34e1e-122">-ServerName</span></span>
<span data-ttu-id="34e1e-123">Określa nazwę serwera AzureSQL, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="34e1e-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="34e1e-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34e1e-124">-Confirm</span></span>
<span data-ttu-id="34e1e-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e1e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e1e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e1e-126">-WhatIf</span></span>
<span data-ttu-id="34e1e-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e1e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e1e-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34e1e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e1e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e1e-129">CommonParameters</span></span>
<span data-ttu-id="34e1e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e1e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e1e-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34e1e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e1e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34e1e-132">INPUTS</span></span>

### <span data-ttu-id="34e1e-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="34e1e-133">System.DateTime</span></span>

### <span data-ttu-id="34e1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="34e1e-134">System.String</span></span>

## <span data-ttu-id="34e1e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34e1e-135">OUTPUTS</span></span>

### <span data-ttu-id="34e1e-136">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="34e1e-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="34e1e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34e1e-137">NOTES</span></span>

## <span data-ttu-id="34e1e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34e1e-138">RELATED LINKS</span></span>

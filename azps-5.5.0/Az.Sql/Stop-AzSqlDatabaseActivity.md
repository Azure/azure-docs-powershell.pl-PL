---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178299"
---
# <span data-ttu-id="7221e-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="7221e-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="7221e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7221e-102">SYNOPSIS</span></span>
<span data-ttu-id="7221e-103">Anuluje asynchroniczną operację aktualizacji w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7221e-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7221e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7221e-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7221e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7221e-105">DESCRIPTION</span></span>
<span data-ttu-id="7221e-106">Polecenie **cmdlet Stop-AzSqlDatabaseActivity** anuluje asynchroniczną operację aktualizacji w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7221e-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7221e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7221e-107">EXAMPLES</span></span>

### <span data-ttu-id="7221e-108">Przykład 1. Anulowanie operacji asynchronicznych aktualizacji w bazie danych</span><span class="sxs-lookup"><span data-stu-id="7221e-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="7221e-109">To polecenie anuluje asynchroniczne aktualizacje w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7221e-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7221e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7221e-110">PARAMETERS</span></span>

### <span data-ttu-id="7221e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7221e-111">-DatabaseName</span></span>
<span data-ttu-id="7221e-112">Określa nazwę bazy danych, dla której to polecenie cmdlet ma stan.</span><span class="sxs-lookup"><span data-stu-id="7221e-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="7221e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7221e-113">-DefaultProfile</span></span>
<span data-ttu-id="7221e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7221e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7221e-115">-PochylićPoolName</span><span class="sxs-lookup"><span data-stu-id="7221e-115">-ElasticPoolName</span></span>
<span data-ttu-id="7221e-116">Nazwa puli elastycznej sql azure.</span><span class="sxs-lookup"><span data-stu-id="7221e-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7221e-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7221e-117">-OperationId</span></span>
<span data-ttu-id="7221e-118">Określa identyfikator operacji, jaka będzie dotyczyć tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7221e-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7221e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7221e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7221e-120">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="7221e-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7221e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7221e-121">-ServerName</span></span>
<span data-ttu-id="7221e-122">Określa nazwę pliku, Microsoft SQL Server hostuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7221e-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="7221e-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7221e-123">-Confirm</span></span>
<span data-ttu-id="7221e-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7221e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7221e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7221e-125">-WhatIf</span></span>
<span data-ttu-id="7221e-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7221e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7221e-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7221e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7221e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7221e-128">CommonParameters</span></span>
<span data-ttu-id="7221e-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7221e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7221e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7221e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7221e-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7221e-131">INPUTS</span></span>

### <span data-ttu-id="7221e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7221e-132">System.String</span></span>

### <span data-ttu-id="7221e-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7221e-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7221e-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7221e-134">OUTPUTS</span></span>

### <span data-ttu-id="7221e-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="7221e-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="7221e-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7221e-136">NOTES</span></span>

## <span data-ttu-id="7221e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7221e-137">RELATED LINKS</span></span>

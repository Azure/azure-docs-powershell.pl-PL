---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f4f3b935aa9303ab38888d6f28f0a89bbdeb6c23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707700"
---
# <span data-ttu-id="9352e-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="9352e-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="9352e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9352e-102">SYNOPSIS</span></span>
<span data-ttu-id="9352e-103">Anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9352e-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="9352e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9352e-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9352e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9352e-105">DESCRIPTION</span></span>
<span data-ttu-id="9352e-106">Polecenie cmdlet **stop-AzSqlDatabaseActivity** anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9352e-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="9352e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9352e-107">EXAMPLES</span></span>

### <span data-ttu-id="9352e-108">Przykład 1. Anuluj operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9352e-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="9352e-109">To polecenie anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="9352e-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="9352e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9352e-110">PARAMETERS</span></span>

### <span data-ttu-id="9352e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9352e-111">-DatabaseName</span></span>
<span data-ttu-id="9352e-112">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="9352e-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="9352e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9352e-113">-DefaultProfile</span></span>
<span data-ttu-id="9352e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9352e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9352e-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9352e-115">-ElasticPoolName</span></span>
<span data-ttu-id="9352e-116">Nazwa puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9352e-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="9352e-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9352e-117">-OperationId</span></span>
<span data-ttu-id="9352e-118">Określa identyfikator operacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9352e-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9352e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9352e-119">-ResourceGroupName</span></span>
<span data-ttu-id="9352e-120">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="9352e-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9352e-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="9352e-121">-ServerName</span></span>
<span data-ttu-id="9352e-122">Określa nazwę programu Microsoft SQL Server, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="9352e-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="9352e-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9352e-123">-Confirm</span></span>
<span data-ttu-id="9352e-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9352e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9352e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9352e-125">-WhatIf</span></span>
<span data-ttu-id="9352e-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9352e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9352e-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9352e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9352e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9352e-128">CommonParameters</span></span>
<span data-ttu-id="9352e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9352e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9352e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9352e-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9352e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9352e-131">INPUTS</span></span>

### <span data-ttu-id="9352e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9352e-132">System.String</span></span>

### <span data-ttu-id="9352e-133">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9352e-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9352e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9352e-134">OUTPUTS</span></span>

### <span data-ttu-id="9352e-135">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="9352e-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="9352e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9352e-136">NOTES</span></span>

## <span data-ttu-id="9352e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9352e-137">RELATED LINKS</span></span>

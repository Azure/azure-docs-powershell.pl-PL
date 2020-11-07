---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895638"
---
# <span data-ttu-id="bfd3a-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="bfd3a-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="bfd3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd3a-103">Anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bfd3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfd3a-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfd3a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bfd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="bfd3a-106">Polecenie cmdlet **stop-AzSqlDatabaseActivity** anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bfd3a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfd3a-107">EXAMPLES</span></span>

### <span data-ttu-id="bfd3a-108">Przykład 1. Anuluj operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="bfd3a-109">To polecenie anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="bfd3a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfd3a-110">PARAMETERS</span></span>

### <span data-ttu-id="bfd3a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bfd3a-111">-DatabaseName</span></span>
<span data-ttu-id="bfd3a-112">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="bfd3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd3a-113">-DefaultProfile</span></span>
<span data-ttu-id="bfd3a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd3a-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bfd3a-115">-ElasticPoolName</span></span>
<span data-ttu-id="bfd3a-116">Nazwa puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="bfd3a-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bfd3a-117">-OperationId</span></span>
<span data-ttu-id="bfd3a-118">Określa identyfikator operacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bfd3a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd3a-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfd3a-120">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="bfd3a-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="bfd3a-121">-ServerName</span></span>
<span data-ttu-id="bfd3a-122">Określa nazwę programu Microsoft SQL Server, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="bfd3a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfd3a-123">-Confirm</span></span>
<span data-ttu-id="bfd3a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfd3a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfd3a-125">-WhatIf</span></span>
<span data-ttu-id="bfd3a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfd3a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfd3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd3a-128">CommonParameters</span></span>
<span data-ttu-id="bfd3a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfd3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd3a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfd3a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd3a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfd3a-131">INPUTS</span></span>

### <span data-ttu-id="bfd3a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bfd3a-132">System.String</span></span>

### <span data-ttu-id="bfd3a-133">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bfd3a-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bfd3a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfd3a-134">OUTPUTS</span></span>

### <span data-ttu-id="bfd3a-135">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="bfd3a-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="bfd3a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfd3a-136">NOTES</span></span>

## <span data-ttu-id="bfd3a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfd3a-137">RELATED LINKS</span></span>

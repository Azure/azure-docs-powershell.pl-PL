---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: af2f10b371eb21558a4b675331ec97f797611d26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543327"
---
# <span data-ttu-id="4dfb6-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="4dfb6-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="4dfb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dfb6-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfb6-103">Anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dfb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dfb6-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dfb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4dfb6-105">DESCRIPTION</span></span>
<span data-ttu-id="4dfb6-106">Polecenie cmdlet **stop-AzureRmSqlDatabaseActivity** anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="4dfb6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dfb6-107">EXAMPLES</span></span>

### <span data-ttu-id="4dfb6-108">Przykład 1. Anuluj operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="4dfb6-109">To polecenie anuluje operację aktualizacji asynchronicznych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="4dfb6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dfb6-110">PARAMETERS</span></span>

### <span data-ttu-id="4dfb6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4dfb6-111">-DatabaseName</span></span>
<span data-ttu-id="4dfb6-112">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="4dfb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfb6-113">-DefaultProfile</span></span>
<span data-ttu-id="4dfb6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfb6-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4dfb6-115">-ElasticPoolName</span></span>
<span data-ttu-id="4dfb6-116">Nazwa puli elastycznej SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="4dfb6-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4dfb6-117">-OperationId</span></span>
<span data-ttu-id="4dfb6-118">Określa identyfikator operacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4dfb6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dfb6-119">-ResourceGroupName</span></span>
<span data-ttu-id="4dfb6-120">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4dfb6-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4dfb6-121">-ServerName</span></span>
<span data-ttu-id="4dfb6-122">Określa nazwę programu Microsoft SQL Server, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="4dfb6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dfb6-123">-Confirm</span></span>
<span data-ttu-id="4dfb6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dfb6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dfb6-125">-WhatIf</span></span>
<span data-ttu-id="4dfb6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dfb6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dfb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfb6-128">CommonParameters</span></span>
<span data-ttu-id="4dfb6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfb6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dfb6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfb6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dfb6-131">INPUTS</span></span>

### <span data-ttu-id="4dfb6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4dfb6-132">System.String</span></span>

### <span data-ttu-id="4dfb6-133">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4dfb6-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4dfb6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dfb6-134">OUTPUTS</span></span>

### <span data-ttu-id="4dfb6-135">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="4dfb6-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="4dfb6-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dfb6-136">NOTES</span></span>

## <span data-ttu-id="4dfb6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dfb6-137">RELATED LINKS</span></span>

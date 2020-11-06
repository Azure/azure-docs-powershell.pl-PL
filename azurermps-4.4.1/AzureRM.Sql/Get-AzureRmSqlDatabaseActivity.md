---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553080"
---
# <span data-ttu-id="aef92-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="aef92-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="aef92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aef92-102">SYNOPSIS</span></span>
<span data-ttu-id="aef92-103">Pobiera stan przeniesień elastycznych baz danych.</span><span class="sxs-lookup"><span data-stu-id="aef92-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aef92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aef92-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aef92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aef92-105">DESCRIPTION</span></span>
<span data-ttu-id="aef92-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseActivity** Pobiera stan elastycznych baz danych, które są przenoszone do lub poza pulę Elastic Database w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="aef92-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="aef92-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aef92-107">EXAMPLES</span></span>

### <span data-ttu-id="aef92-108">Przykład 1: uzyskiwanie statusu dla wszystkich wystąpień bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="aef92-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="aef92-109">To polecenie zwraca stan operacji wszystkich wystąpień bazy danych SQL w puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="aef92-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="aef92-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aef92-110">PARAMETERS</span></span>

### <span data-ttu-id="aef92-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aef92-111">-DatabaseName</span></span>
<span data-ttu-id="aef92-112">Określa nazwę bazy danych, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="aef92-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="aef92-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="aef92-113">-ElasticPoolName</span></span>
<span data-ttu-id="aef92-114">Określa nazwę puli Elastic Database, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="aef92-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="aef92-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="aef92-115">-OperationId</span></span>
<span data-ttu-id="aef92-116">Określa identyfikator operacji, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef92-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aef92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef92-117">-ResourceGroupName</span></span>
<span data-ttu-id="aef92-118">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="aef92-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="aef92-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="aef92-119">-ServerName</span></span>
<span data-ttu-id="aef92-120">Określa nazwę programu Microsoft SQL Server obsługującego pulę Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="aef92-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="aef92-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aef92-121">-Confirm</span></span>
<span data-ttu-id="aef92-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef92-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef92-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef92-123">-WhatIf</span></span>
<span data-ttu-id="aef92-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef92-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef92-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aef92-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef92-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef92-126">-DefaultProfile</span></span>
<span data-ttu-id="aef92-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aef92-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aef92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef92-128">CommonParameters</span></span>
<span data-ttu-id="aef92-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef92-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aef92-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef92-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aef92-131">INPUTS</span></span>

## <span data-ttu-id="aef92-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aef92-132">OUTPUTS</span></span>

### <span data-ttu-id="aef92-133">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="aef92-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="aef92-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aef92-134">NOTES</span></span>

## <span data-ttu-id="aef92-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aef92-135">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: f2229fa904144b0dd95a054da95db99600963406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542840"
---
# <span data-ttu-id="2ecf6-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2ecf6-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="2ecf6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ecf6-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecf6-103">Pobiera elastyczną bazę danych w puli elastycznej i jej wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ecf6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ecf6-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ecf6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ecf6-105">DESCRIPTION</span></span>
<span data-ttu-id="2ecf6-106">Polecenie cmdlet **Get-AzureRmSqlElasticPoolDatabase** pobiera elastyczną bazę danych w puli elastycznej oraz wartości ich właściwości.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="2ecf6-107">W usłudze Azure SQL Database można określić nazwę Elastic Database, aby wyświetlić wartości właściwości tylko tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="2ecf6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ecf6-108">EXAMPLES</span></span>

### <span data-ttu-id="2ecf6-109">Przykład 1: pobieranie wszystkich baz danych w elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="2ecf6-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2ecf6-110">To polecenie pobiera wszystkie bazy danych z puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="2ecf6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ecf6-111">PARAMETERS</span></span>

### <span data-ttu-id="2ecf6-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ecf6-112">-DatabaseName</span></span>
<span data-ttu-id="2ecf6-113">Określa nazwę bazy danych SQL, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ecf6-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2ecf6-114">-ElasticPoolName</span></span>
<span data-ttu-id="2ecf6-115">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="2ecf6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ecf6-116">-ResourceGroupName</span></span>
<span data-ttu-id="2ecf6-117">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="2ecf6-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2ecf6-118">-ServerName</span></span>
<span data-ttu-id="2ecf6-119">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="2ecf6-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ecf6-120">-Confirm</span></span>
<span data-ttu-id="2ecf6-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ecf6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ecf6-122">-WhatIf</span></span>
<span data-ttu-id="2ecf6-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ecf6-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ecf6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecf6-125">-DefaultProfile</span></span>
<span data-ttu-id="2ecf6-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ecf6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecf6-127">CommonParameters</span></span>
<span data-ttu-id="2ecf6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ecf6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecf6-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ecf6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecf6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ecf6-130">INPUTS</span></span>

## <span data-ttu-id="2ecf6-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ecf6-131">OUTPUTS</span></span>

### <span data-ttu-id="2ecf6-132">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2ecf6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2ecf6-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ecf6-133">NOTES</span></span>

## <span data-ttu-id="2ecf6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ecf6-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ecf6-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ecf6-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2ecf6-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2ecf6-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="2ecf6-137">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ecf6-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2ecf6-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ecf6-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2ecf6-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2ecf6-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


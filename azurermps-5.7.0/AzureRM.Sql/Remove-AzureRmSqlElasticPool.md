---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: a6b5b21b8911aa8d156ced40476d1b0ecadad361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542215"
---
# <span data-ttu-id="7a153-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a153-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="7a153-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a153-102">SYNOPSIS</span></span>
<span data-ttu-id="7a153-103">Usuwa pulę Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="7a153-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a153-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a153-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a153-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a153-105">DESCRIPTION</span></span>
<span data-ttu-id="7a153-106">Polecenie cmdlet **Remove-AzureRmSqlElasticPool** usuwa pulę elastyczną bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7a153-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="7a153-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a153-107">EXAMPLES</span></span>

### <span data-ttu-id="7a153-108">Przykład 1: usuwanie elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="7a153-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="7a153-109">To polecenie usuwa elastyczną pulę o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="7a153-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="7a153-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a153-110">PARAMETERS</span></span>

### <span data-ttu-id="7a153-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a153-111">-DefaultProfile</span></span>
<span data-ttu-id="7a153-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7a153-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a153-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7a153-113">-ElasticPoolName</span></span>
<span data-ttu-id="7a153-114">Określa nazwę puli elastycznej, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="7a153-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a153-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a153-115">-Force</span></span>
<span data-ttu-id="7a153-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7a153-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a153-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a153-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a153-118">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="7a153-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a153-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7a153-119">-ServerName</span></span>
<span data-ttu-id="7a153-120">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="7a153-120">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a153-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a153-121">-Confirm</span></span>
<span data-ttu-id="7a153-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a153-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a153-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a153-123">-WhatIf</span></span>
<span data-ttu-id="7a153-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a153-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a153-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a153-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a153-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a153-126">CommonParameters</span></span>
<span data-ttu-id="7a153-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a153-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a153-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a153-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a153-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a153-129">INPUTS</span></span>

### <span data-ttu-id="7a153-130">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="7a153-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7a153-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a153-131">OUTPUTS</span></span>

### <span data-ttu-id="7a153-132">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="7a153-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7a153-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a153-133">NOTES</span></span>

## <span data-ttu-id="7a153-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a153-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a153-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a153-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7a153-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7a153-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="7a153-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="7a153-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="7a153-138">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a153-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7a153-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7a153-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7a153-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="7a153-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



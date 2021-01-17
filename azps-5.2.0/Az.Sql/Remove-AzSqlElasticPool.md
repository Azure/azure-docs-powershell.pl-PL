---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369621"
---
# <span data-ttu-id="1cbcc-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1cbcc-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="1cbcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1cbcc-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbcc-103">Usuwa pulę Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="1cbcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1cbcc-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cbcc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1cbcc-105">DESCRIPTION</span></span>
<span data-ttu-id="1cbcc-106">Polecenie cmdlet **Remove-AzSqlElasticPool** usuwa pulę elastyczną bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="1cbcc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1cbcc-107">EXAMPLES</span></span>

### <span data-ttu-id="1cbcc-108">Przykład 1: usuwanie elastycznej puli</span><span class="sxs-lookup"><span data-stu-id="1cbcc-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="1cbcc-109">To polecenie usuwa elastyczną pulę o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="1cbcc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1cbcc-110">PARAMETERS</span></span>

### <span data-ttu-id="1cbcc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbcc-111">-DefaultProfile</span></span>
<span data-ttu-id="1cbcc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1cbcc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cbcc-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1cbcc-113">-ElasticPoolName</span></span>
<span data-ttu-id="1cbcc-114">Określa nazwę puli elastycznej, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbcc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1cbcc-115">-Force</span></span>
<span data-ttu-id="1cbcc-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1cbcc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbcc-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cbcc-118">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="1cbcc-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1cbcc-119">-ServerName</span></span>
<span data-ttu-id="1cbcc-120">Określa nazwę serwera obsługującego pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="1cbcc-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1cbcc-121">-Confirm</span></span>
<span data-ttu-id="1cbcc-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cbcc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cbcc-123">-WhatIf</span></span>
<span data-ttu-id="1cbcc-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cbcc-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cbcc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbcc-126">CommonParameters</span></span>
<span data-ttu-id="1cbcc-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbcc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbcc-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cbcc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbcc-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1cbcc-129">INPUTS</span></span>

### <span data-ttu-id="1cbcc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1cbcc-130">System.String</span></span>

## <span data-ttu-id="1cbcc-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1cbcc-131">OUTPUTS</span></span>

### <span data-ttu-id="1cbcc-132">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="1cbcc-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="1cbcc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1cbcc-133">NOTES</span></span>

## <span data-ttu-id="1cbcc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1cbcc-134">RELATED LINKS</span></span>

[<span data-ttu-id="1cbcc-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1cbcc-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="1cbcc-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="1cbcc-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="1cbcc-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="1cbcc-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="1cbcc-138">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1cbcc-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="1cbcc-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1cbcc-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="1cbcc-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1cbcc-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



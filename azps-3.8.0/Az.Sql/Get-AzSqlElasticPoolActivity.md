---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896573"
---
# <span data-ttu-id="33bc9-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="33bc9-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="33bc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="33bc9-103">Pobiera stan operacji z puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="33bc9-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="33bc9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33bc9-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33bc9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="33bc9-106">Polecenie cmdlet **Get-AzSqlElasticPoolActivity** Pobiera stan operacji z puli elastycznej dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="33bc9-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="33bc9-107">Możesz sprawdzić stan tworzenia puli i aktualizacji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="33bc9-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="33bc9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33bc9-108">EXAMPLES</span></span>

### <span data-ttu-id="33bc9-109">Przykład 1: uzyskiwanie stanu operacji dla puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="33bc9-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="33bc9-110">To polecenie uzyskuje stan operacji dla puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="33bc9-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="33bc9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33bc9-111">PARAMETERS</span></span>

### <span data-ttu-id="33bc9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bc9-112">-DefaultProfile</span></span>
<span data-ttu-id="33bc9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="33bc9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33bc9-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="33bc9-114">-ElasticPoolName</span></span>
<span data-ttu-id="33bc9-115">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="33bc9-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="33bc9-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="33bc9-116">-OperationId</span></span>
<span data-ttu-id="33bc9-117">Identyfikator operacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="33bc9-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="33bc9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33bc9-118">-ResourceGroupName</span></span>
<span data-ttu-id="33bc9-119">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="33bc9-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="33bc9-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="33bc9-120">-ServerName</span></span>
<span data-ttu-id="33bc9-121">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="33bc9-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="33bc9-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33bc9-122">-Confirm</span></span>
<span data-ttu-id="33bc9-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33bc9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33bc9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33bc9-124">-WhatIf</span></span>
<span data-ttu-id="33bc9-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33bc9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33bc9-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33bc9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33bc9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bc9-127">CommonParameters</span></span>
<span data-ttu-id="33bc9-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33bc9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bc9-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33bc9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bc9-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33bc9-130">INPUTS</span></span>

### <span data-ttu-id="33bc9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="33bc9-131">System.String</span></span>

### <span data-ttu-id="33bc9-132">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="33bc9-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="33bc9-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33bc9-133">OUTPUTS</span></span>

### <span data-ttu-id="33bc9-134">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="33bc9-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="33bc9-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33bc9-135">NOTES</span></span>

## <span data-ttu-id="33bc9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33bc9-136">RELATED LINKS</span></span>

[<span data-ttu-id="33bc9-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33bc9-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="33bc9-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="33bc9-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="33bc9-139">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33bc9-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="33bc9-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33bc9-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="33bc9-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33bc9-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)



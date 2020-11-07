---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: f5e7455a253c86fe363b72c5d4c0e8ff47b96f56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717896"
---
# <span data-ttu-id="ffa0a-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ffa0a-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="ffa0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffa0a-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa0a-103">Pobiera stan operacji z puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffa0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffa0a-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffa0a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffa0a-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa0a-106">Polecenie cmdlet **Get-AzureRmSqlElasticPoolActivity** Pobiera stan operacji z puli elastycznej dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="ffa0a-107">Możesz sprawdzić stan tworzenia puli i aktualizacji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="ffa0a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffa0a-108">EXAMPLES</span></span>

### <span data-ttu-id="ffa0a-109">Przykład 1: uzyskiwanie stanu operacji dla puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="ffa0a-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ffa0a-110">To polecenie uzyskuje stan operacji dla puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="ffa0a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffa0a-111">PARAMETERS</span></span>

### <span data-ttu-id="ffa0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa0a-112">-DefaultProfile</span></span>
<span data-ttu-id="ffa0a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ffa0a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffa0a-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ffa0a-114">-ElasticPoolName</span></span>
<span data-ttu-id="ffa0a-115">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="ffa0a-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ffa0a-116">-OperationId</span></span>
<span data-ttu-id="ffa0a-117">Identyfikator operacji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="ffa0a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa0a-118">-ResourceGroupName</span></span>
<span data-ttu-id="ffa0a-119">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="ffa0a-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ffa0a-120">-ServerName</span></span>
<span data-ttu-id="ffa0a-121">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="ffa0a-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffa0a-122">-Confirm</span></span>
<span data-ttu-id="ffa0a-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa0a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa0a-124">-WhatIf</span></span>
<span data-ttu-id="ffa0a-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa0a-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa0a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa0a-127">CommonParameters</span></span>
<span data-ttu-id="ffa0a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa0a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa0a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa0a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa0a-130">INPUTS</span></span>

### <span data-ttu-id="ffa0a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ffa0a-131">System.String</span></span>

### <span data-ttu-id="ffa0a-132">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ffa0a-132">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ffa0a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffa0a-133">OUTPUTS</span></span>

### <span data-ttu-id="ffa0a-134">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="ffa0a-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="ffa0a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffa0a-135">NOTES</span></span>

## <span data-ttu-id="ffa0a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffa0a-136">RELATED LINKS</span></span>

[<span data-ttu-id="ffa0a-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ffa0a-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ffa0a-138">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ffa0a-138">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="ffa0a-139">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ffa0a-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ffa0a-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ffa0a-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ffa0a-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ffa0a-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)



---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 88052c9f47359e0080e193f5a2dbb1004b48b0e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717302"
---
# <span data-ttu-id="646a2-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="646a2-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="646a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="646a2-102">SYNOPSIS</span></span>
<span data-ttu-id="646a2-103">Pobiera stan operacji z puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="646a2-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="646a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="646a2-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="646a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="646a2-105">DESCRIPTION</span></span>
<span data-ttu-id="646a2-106">Polecenie cmdlet **Get-AzureRmSqlElasticPoolActivity** Pobiera stan operacji z puli elastycznej dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="646a2-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="646a2-107">Możesz sprawdzić stan tworzenia puli i aktualizacji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="646a2-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="646a2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="646a2-108">EXAMPLES</span></span>

### <span data-ttu-id="646a2-109">Przykład 1: uzyskiwanie stanu operacji dla puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="646a2-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="646a2-110">To polecenie uzyskuje stan operacji dla puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="646a2-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="646a2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="646a2-111">PARAMETERS</span></span>

### <span data-ttu-id="646a2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646a2-112">-DefaultProfile</span></span>
<span data-ttu-id="646a2-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="646a2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="646a2-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="646a2-114">-ElasticPoolName</span></span>
<span data-ttu-id="646a2-115">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="646a2-115">Specifies the name of an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="646a2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="646a2-116">-ResourceGroupName</span></span>
<span data-ttu-id="646a2-117">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="646a2-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="646a2-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="646a2-118">-ServerName</span></span>
<span data-ttu-id="646a2-119">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="646a2-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="646a2-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="646a2-120">-Confirm</span></span>
<span data-ttu-id="646a2-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="646a2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="646a2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646a2-122">-WhatIf</span></span>
<span data-ttu-id="646a2-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="646a2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="646a2-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="646a2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="646a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646a2-125">CommonParameters</span></span>
<span data-ttu-id="646a2-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646a2-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="646a2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646a2-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="646a2-128">INPUTS</span></span>

### <span data-ttu-id="646a2-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="646a2-129">None</span></span>
<span data-ttu-id="646a2-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="646a2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="646a2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="646a2-131">OUTPUTS</span></span>

### <span data-ttu-id="646a2-132">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="646a2-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="646a2-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="646a2-133">NOTES</span></span>

## <span data-ttu-id="646a2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="646a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="646a2-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="646a2-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="646a2-136">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="646a2-136">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="646a2-137">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="646a2-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="646a2-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="646a2-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="646a2-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="646a2-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)



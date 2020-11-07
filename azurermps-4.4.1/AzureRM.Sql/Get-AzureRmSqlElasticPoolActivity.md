---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: d78b2fafb6c633c8a0276193e9e42677de814ff3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716867"
---
# <span data-ttu-id="57ac5-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="57ac5-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="57ac5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="57ac5-103">Pobiera stan operacji z puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="57ac5-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57ac5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57ac5-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57ac5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="57ac5-106">Polecenie cmdlet **Get-AzureRmSqlElasticPoolActivity** Pobiera stan operacji z puli elastycznej dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="57ac5-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="57ac5-107">Możesz sprawdzić stan tworzenia puli i aktualizacji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="57ac5-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="57ac5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57ac5-108">EXAMPLES</span></span>

### <span data-ttu-id="57ac5-109">Przykład 1: uzyskiwanie stanu operacji dla puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="57ac5-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="57ac5-110">To polecenie uzyskuje stan operacji dla puli elastycznej o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="57ac5-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="57ac5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57ac5-111">PARAMETERS</span></span>

### <span data-ttu-id="57ac5-112">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="57ac5-112">-ElasticPoolName</span></span>
<span data-ttu-id="57ac5-113">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="57ac5-113">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="57ac5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ac5-114">-ResourceGroupName</span></span>
<span data-ttu-id="57ac5-115">Określa nazwę grupy zasobów, do której jest przypisana elastyczna Pula.</span><span class="sxs-lookup"><span data-stu-id="57ac5-115">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="57ac5-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="57ac5-116">-ServerName</span></span>
<span data-ttu-id="57ac5-117">Określa nazwę serwera zawierającego elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="57ac5-117">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="57ac5-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57ac5-118">-Confirm</span></span>
<span data-ttu-id="57ac5-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57ac5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ac5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ac5-120">-WhatIf</span></span>
<span data-ttu-id="57ac5-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57ac5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ac5-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57ac5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ac5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ac5-123">-DefaultProfile</span></span>
<span data-ttu-id="57ac5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57ac5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ac5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ac5-125">CommonParameters</span></span>
<span data-ttu-id="57ac5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ac5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ac5-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ac5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ac5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57ac5-128">INPUTS</span></span>

## <span data-ttu-id="57ac5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57ac5-129">OUTPUTS</span></span>

### <span data-ttu-id="57ac5-130">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="57ac5-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="57ac5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57ac5-131">NOTES</span></span>

## <span data-ttu-id="57ac5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57ac5-132">RELATED LINKS</span></span>

[<span data-ttu-id="57ac5-133">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ac5-133">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="57ac5-134">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="57ac5-134">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="57ac5-135">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ac5-135">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="57ac5-136">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ac5-136">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="57ac5-137">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="57ac5-137">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)



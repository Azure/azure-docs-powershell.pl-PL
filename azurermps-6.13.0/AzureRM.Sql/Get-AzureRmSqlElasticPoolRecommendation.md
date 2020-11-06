---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendation.md
ms.openlocfilehash: 0769824bc0b50641f7b73cb530dde0a5f30bf7ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544776"
---
# <span data-ttu-id="72115-101">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="72115-101">Get-AzureRmSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="72115-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72115-102">SYNOPSIS</span></span>
<span data-ttu-id="72115-103">Pobiera elastyczne rekomendacje.</span><span class="sxs-lookup"><span data-stu-id="72115-103">Gets elastic pool recommendations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72115-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72115-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72115-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72115-105">DESCRIPTION</span></span>
<span data-ttu-id="72115-106">Polecenie cmdlet **Get-AzureRmSqlElasticPoolRecommendation** umożliwia pobieranie elastycznych rekomendacji dla serwera.</span><span class="sxs-lookup"><span data-stu-id="72115-106">The **Get-AzureRmSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="72115-107">Zalecenia te obejmują następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="72115-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="72115-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="72115-108">DatabaseCollection.</span></span> <span data-ttu-id="72115-109">Kolekcja nazw baz danych należących do puli.</span><span class="sxs-lookup"><span data-stu-id="72115-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="72115-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="72115-110">DatabaseDtuMin.</span></span> <span data-ttu-id="72115-111">Gwarancja jednostki transmisji danych (DTU) dla baz danych w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72115-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="72115-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="72115-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="72115-113">WPR (DTU Cap) dla baz danych w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72115-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="72115-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="72115-114">Dtu.</span></span> <span data-ttu-id="72115-115">Gwarancja jednostek DTU dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72115-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="72115-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="72115-116">StorageMb.</span></span> <span data-ttu-id="72115-117">Miejsce do magazynowania w megabajtach dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72115-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="72115-118">Edition.</span><span class="sxs-lookup"><span data-stu-id="72115-118">Edition.</span></span> <span data-ttu-id="72115-119">Wersja dla puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72115-119">Edition for the elastic pool.</span></span> <span data-ttu-id="72115-120">Dopuszczalne wartości tego parametru to: Basic, standard i Premium.</span><span class="sxs-lookup"><span data-stu-id="72115-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="72115-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="72115-121">IncludeAllDatabases.</span></span> <span data-ttu-id="72115-122">Wskazuje, czy zostaną zwrócone wszystkie bazy danych w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72115-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="72115-123">Nazwę.</span><span class="sxs-lookup"><span data-stu-id="72115-123">Name.</span></span> <span data-ttu-id="72115-124">Nazwa puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="72115-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="72115-125">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72115-125">EXAMPLES</span></span>

### <span data-ttu-id="72115-126">Przykład 1: uzyskiwanie rekomendacji dla serwera</span><span class="sxs-lookup"><span data-stu-id="72115-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="72115-127">To polecenie uzyskuje rekomendacje dotyczące puli elastycznej dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="72115-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="72115-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72115-128">PARAMETERS</span></span>

### <span data-ttu-id="72115-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72115-129">-DefaultProfile</span></span>
<span data-ttu-id="72115-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="72115-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72115-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72115-131">-ResourceGroupName</span></span>
<span data-ttu-id="72115-132">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="72115-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="72115-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="72115-133">-ServerName</span></span>
<span data-ttu-id="72115-134">Określa nazwę serwera, dla którego jest pobierana rekomendacja tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72115-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="72115-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72115-135">-Confirm</span></span>
<span data-ttu-id="72115-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72115-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72115-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72115-137">-WhatIf</span></span>
<span data-ttu-id="72115-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72115-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72115-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72115-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72115-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72115-140">CommonParameters</span></span>
<span data-ttu-id="72115-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72115-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72115-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72115-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72115-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72115-143">INPUTS</span></span>

### <span data-ttu-id="72115-144">System. String</span><span class="sxs-lookup"><span data-stu-id="72115-144">System.String</span></span>

## <span data-ttu-id="72115-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72115-145">OUTPUTS</span></span>

### <span data-ttu-id="72115-146">Microsoft. Azure. Management. SQL. LegacySdk. MODELES. UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="72115-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="72115-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72115-147">NOTES</span></span>

## <span data-ttu-id="72115-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72115-148">RELATED LINKS</span></span>

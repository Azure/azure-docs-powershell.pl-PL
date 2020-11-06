---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpooladvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7b4d445ede7bae59431707f3ff6bc587effde21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547848"
---
# <span data-ttu-id="f9d30-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f9d30-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="f9d30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9d30-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d30-103">Aktualizuje stan automatycznego wykonania klasyfikatora Elastic Pool SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d30-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9d30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9d30-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9d30-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9d30-105">DESCRIPTION</span></span>
<span data-ttu-id="f9d30-106">Polecenie cmdlet **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** ustawia właściwość AutoExecute dla klasyfikatora Elastic Pool SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d30-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="f9d30-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9d30-107">EXAMPLES</span></span>

### <span data-ttu-id="f9d30-108">Przykład 1: Włączanie automatycznego wykonywania dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="f9d30-108">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
'Enabled'ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : ElasticPool
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="f9d30-109">To polecenie ustawia stan automatycznego wykonania klasyfikatora o nazwie "Moja indeks" na włączony.</span><span class="sxs-lookup"><span data-stu-id="f9d30-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="f9d30-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9d30-110">PARAMETERS</span></span>

### <span data-ttu-id="f9d30-111">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="f9d30-111">-AdvisorName</span></span>
<span data-ttu-id="f9d30-112">Określa nazwę klasyfikatora, dla którego to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="f9d30-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d30-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f9d30-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="f9d30-114">Określa nową wartość, na którą to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="f9d30-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="f9d30-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f9d30-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9d30-116">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="f9d30-116">Enabled</span></span>
- <span data-ttu-id="f9d30-117">Łącza</span><span class="sxs-lookup"><span data-stu-id="f9d30-117">Disabled</span></span>
- <span data-ttu-id="f9d30-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="f9d30-118">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d30-119">-DefaultProfile</span></span>
<span data-ttu-id="f9d30-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f9d30-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9d30-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f9d30-121">-ElasticPoolName</span></span>
<span data-ttu-id="f9d30-122">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="f9d30-122">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d30-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d30-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9d30-124">Określa nazwę grupy zasobów serwera, która zawiera tę pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="f9d30-124">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="f9d30-125">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f9d30-125">-ServerName</span></span>
<span data-ttu-id="f9d30-126">Określa nazwę serwera, na którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="f9d30-126">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d30-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9d30-127">-Confirm</span></span>
<span data-ttu-id="f9d30-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d30-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d30-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d30-129">-WhatIf</span></span>
<span data-ttu-id="f9d30-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d30-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d30-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9d30-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d30-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d30-132">CommonParameters</span></span>
<span data-ttu-id="f9d30-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d30-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d30-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9d30-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d30-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9d30-135">INPUTS</span></span>

### <span data-ttu-id="f9d30-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f9d30-136">None</span></span>
<span data-ttu-id="f9d30-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f9d30-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9d30-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9d30-138">OUTPUTS</span></span>

### <span data-ttu-id="f9d30-139">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="f9d30-139">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="f9d30-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9d30-140">NOTES</span></span>
* <span data-ttu-id="f9d30-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elastyczna Pula, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="f9d30-141">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="f9d30-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9d30-142">RELATED LINKS</span></span>

[<span data-ttu-id="f9d30-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="f9d30-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="f9d30-144">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f9d30-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BAA0781E-DC02-4AAF-A039-9B71B67E6696
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 5a03216c0a1d507731be75b63277cdd46e3be46d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542804"
---
# <span data-ttu-id="64397-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="64397-101">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="64397-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64397-102">SYNOPSIS</span></span>
<span data-ttu-id="64397-103">Aktualizuje stan automatycznego wykonania klasyfikatora Elastic Pool SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="64397-103">Updates auto execute status of an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64397-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64397-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -ElasticPoolName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64397-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64397-105">DESCRIPTION</span></span>
<span data-ttu-id="64397-106">Polecenie cmdlet **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** ustawia właściwość AutoExecute dla klasyfikatora Elastic Pool SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="64397-106">The **Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus** cmdlet sets auto execute property for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="64397-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64397-107">EXAMPLES</span></span>

### <span data-ttu-id="64397-108">Przykład 1: Włączanie automatycznego wykonywania dla klasyfikatora</span><span class="sxs-lookup"><span data-stu-id="64397-108">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="64397-109">To polecenie ustawia stan automatycznego wykonania klasyfikatora o nazwie "Moja indeks" na włączony.</span><span class="sxs-lookup"><span data-stu-id="64397-109">This command sets the auto execute status of an advisor named CreateIndex to enabled.</span></span>

## <span data-ttu-id="64397-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64397-110">PARAMETERS</span></span>

### <span data-ttu-id="64397-111">-Klasyfikatorname</span><span class="sxs-lookup"><span data-stu-id="64397-111">-AdvisorName</span></span>
<span data-ttu-id="64397-112">Określa nazwę klasyfikatora, dla którego to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="64397-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="64397-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="64397-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="64397-114">Określa nową wartość, na którą to polecenie cmdlet aktualizuje stan automatycznego wykonywania.</span><span class="sxs-lookup"><span data-stu-id="64397-114">Specifies a new value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="64397-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="64397-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64397-116">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="64397-116">Enabled</span></span>
- <span data-ttu-id="64397-117">Łącza</span><span class="sxs-lookup"><span data-stu-id="64397-117">Disabled</span></span>
- <span data-ttu-id="64397-118">Domyślne</span><span class="sxs-lookup"><span data-stu-id="64397-118">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64397-119">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="64397-119">-ElasticPoolName</span></span>
<span data-ttu-id="64397-120">Określa nazwę puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="64397-120">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="64397-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64397-121">-ResourceGroupName</span></span>
<span data-ttu-id="64397-122">Określa nazwę grupy zasobów serwera, która zawiera tę pulę elastyczną.</span><span class="sxs-lookup"><span data-stu-id="64397-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="64397-123">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="64397-123">-ServerName</span></span>
<span data-ttu-id="64397-124">Określa nazwę serwera, na którym znajduje się pula elastyczna.</span><span class="sxs-lookup"><span data-stu-id="64397-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="64397-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64397-125">-Confirm</span></span>
<span data-ttu-id="64397-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64397-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64397-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64397-127">-WhatIf</span></span>
<span data-ttu-id="64397-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64397-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64397-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64397-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64397-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64397-130">-DefaultProfile</span></span>
<span data-ttu-id="64397-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64397-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64397-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64397-132">CommonParameters</span></span>
<span data-ttu-id="64397-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64397-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64397-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64397-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64397-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64397-135">INPUTS</span></span>

## <span data-ttu-id="64397-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64397-136">OUTPUTS</span></span>

### <span data-ttu-id="64397-137">Microsoft. Azure. Commands. SQL. Advisor. model. AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="64397-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="64397-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64397-138">NOTES</span></span>
* <span data-ttu-id="64397-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, elastyczna Pula, MSSQL, Doradca</span><span class="sxs-lookup"><span data-stu-id="64397-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, elastic pool, mssql, advisor</span></span>

## <span data-ttu-id="64397-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64397-140">RELATED LINKS</span></span>

[<span data-ttu-id="64397-141">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="64397-141">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="64397-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="64397-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
